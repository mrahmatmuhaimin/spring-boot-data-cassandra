# Spring Boot Cassandra CRUD - Restful CRUD API
Link youtube : https://youtu.be/-18J0JNb6s8

## Kelompok 6
- Muhammad Rahmat Muhaimin (1207050078)
- Muhammad Aqsal Sirulah Sodik (1207050068)
- Munazir Dzuana Setiawan (1207050085)

## Cara Instal 
Kami anggap anda sudah menginstal Docker desktop, Maven, dan Java(8) minimum pada komputer anda
- Clone repository: `git clone https://github.com/mrahmatmuhaimin/spring-boot-data-cassandra.git`
- masuk ke filenya : `cd spring-boot-data-cassandra`
- jalankan docker compose : `docker compose -f docker-compose.yml up -d`

## Cara Setup
1. Akses Cassandra : `docker-compose exec cassandra bash`
2. Masuk ke shell cassandra : `cqlsh`
3. buat keyspace : `create keyspace kelompok6 with replication={'class':'SimpleStrategy', 'replication_factor':1};`
4. masuk ke keyspace : `use kelompok6`
5. Buat Table :`CREATE TABLE tutorial(
   id timeuuid PRIMARY KEY,
   title text,
   description text,
   published boolean
);`

## Run Spring Boot application
```
mvn spring-boot:run
```

## Endpoint
| Methode | Urls | Actions |
| --- |:--------:| --------:|
| Post | /api/tutorials | Buat Data baru |
| Get | /api/tutorials | Tampilkan semua Data |
| Get | /api/tutorials/:id | Tampilkan Data sesuai id |
| Put | /api/tutorials/:id | Update Data sesuai id |
| Delete | /api/tutorials/:id | Hapus Data sesuai id |
| Delete | /api/tutorials/ | Hapus semua Data |
| Get | /api/tutorials/published | Tampilkan Data published |

## Screenshot
