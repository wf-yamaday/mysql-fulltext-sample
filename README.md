# MySQL fulltext search sample

百人一首のデータはこちらから取得しています．
> https://github.com/nyoronjp/Ogura_Hyakunin_Isshu.csv

# 実行環境

- MySQL 8.0
- Docker version 19.03.13
- docker-compose version 1.27.4

```bash
docker exec -it n-gram_db_1 bin/bash -c "mysql -u root -p"
```

```sql
SELECT * FROM ogura WHERE MATCH (above) AGAINST ('君がため');
```
