## MySQL audit

1. `docker-compose down -v && docker-compose up --abort-on-container-exit`
2. `docker-compose exec db sh -c "tail -f /var/lib/mysql/audit.log | grep test_user`
3. `mysql -h 127.0.0.1 -u test_user -ptest_password -e "SHOW VARIABLES LIKE 'audit_log_%'"`
