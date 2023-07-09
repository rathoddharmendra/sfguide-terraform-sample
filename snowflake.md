CREATE USER "tf-snow" RSA_PUBLIC_KEY='MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA2zE+GVL0lxKvjxzrxq12H9GPee0u681e1Tbvx95OdVxXX9GmvzLeo5+qq0dRuqpaRtUiI7xumo3reqcJYXhW+j5rPPS5G+rvogEY1x7pKImmnpD5onPI55Ye8vNypg2q8N6wbrYjMgYGXT7qQ37w2bNCPBYbVVkR4ukC+tjrTSuwlvfLo8PT9wWX2/YxPYXFLtPUkwkYmyIVsWycA5ngeZFP9MXTJK2+VRTGMmg7usmBJ4QscEcSzARh1y6xc+D8XQT+0gYC/SvMyjQ9quzZZYUEFedddKzfJwIGZ7s7KVQgZtaN9S1IRQZvZP/130+PVm5r7vkTJn9mrVo3PZxEQQIDAQAB' DEFAULT_ROLE=PUBLIC MUST_CHANGE_PASSWORD=FALSE;

GRANT ROLE SYSADMIN TO USER "tf-snow";
GRANT ROLE SECURITYADMIN TO USER "tf-snow";

YOUR_ACCOUNT_LOCATOR: ZB25708
YOUR_SNOWFLAKE_REGION_ID: AWS_AP_SOUTH_1


export SNOWFLAKE_USER="tf-snow" && export SNOWFLAKE_PRIVATE_KEY_PATH="~/.ssh/snowflake_tf_snow_key.p8" && export SNOWFLAKE_ACCOUNT="ZB25708" && export SNOWFLAKE_REGION="AWS_AP_SOUTH_1"


$ git checkout -b dbwh
$ git add main.tf
$ git add .gitignore
$ git commit -m "Add Database and Warehouse"
$ git push origin HEAD

https://zb25708.ap-south-1.aws.snowflakecomputing.com/