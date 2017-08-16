# openfalcon-ui


- 修改dashboard/rrd/config.py,修改之后重启服务
    - API_ADDR = os.environ.get("API_ADDR","http://1.1.1.1:8080/api/v1")

    - PORTAL_DB_HOST = os.environ.get("PORTAL_DB_HOST","2.2.2.2")
    - PORTAL_DB_PORT = int(os.environ.get("PORTAL_DB_PORT",3306))
    - PORTAL_DB_USER = os.environ.get("PORTAL_DB_USER","root")
    - PORTAL_DB_PASS = os.environ.get("PORTAL_DB_PASS","123456")
    - PORTAL_DB_NAME = os.environ.get("PORTAL_DB_NAME","falcon_portal")

    - ALARM_DB_HOST = os.environ.get("ALARM_DB_HOST","2.2.2.2")
    - ALARM_DB_PORT = int(os.environ.get("ALARM_DB_PORT",3306))
    - ALARM_DB_USER = os.environ.get("ALARM_DB_USER","openfalcon")
    - ALARM_DB_PASS = os.environ.get("ALARM_DB_PASS","123456")
    - ALARM_DB_NAME = os.environ.get("ALARM_DB_NAME","alarms")



- 登陆mysql
    - mysql -h 1.1.1.1 -P3306 -uroot -p123456
    - use uic;
    - #获取需要成为admin的id
    - select * from user;
    - #修改为uid为1的用户为admin
    - update user set user.role=1 where id=1;

