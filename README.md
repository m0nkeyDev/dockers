# 🗄️ Multi-Database Docker Environment

This repository provides Docker container setups for both SQL, NoSQL, and Vector database environments, designed to simplify local development and testing.

## 📁 Project Structure

```

./
├── LICENSE
├── README.md
└── databases
├── nosql
│   └── redis
│       └── docker-compose.yml
├── sql
│   └── postgresql
│       └── docker-compose.yml
├── vector
│   └── qdrant
│       └── docker-compose.yml

````

---

## 🧩 Included Databases

### 🐘 PostgreSQL + pgAdmin

Location: `./databases/sql/postgresql/docker-compose.yml`

Includes:

- **PostgreSQL** with custom credentials and persistent volume.
- **pgAdmin 4** web UI available at `http://localhost:8080`.

#### Default Credentials:

- PostgreSQL:
  - User: `m0nkeyDev`
  - Database: `psql001`
  - Password: `pgpassword`

- pgAdmin:
  - Email: `m0nkeyDev@m0nkeyDev.com`
  - Password: `pgadmin_password`

---

### 🔴 Redis + Redis Commander

Location: `./databases/nosql/redis/docker-compose.yml`

Includes:

- **Redis** with persistent volume.
- **Redis Commander**, a web-based UI available at `http://localhost:8081`.

Automatically configured to connect to the Redis container via service name (`redis`).

---

## 🚀 How to Use

### PostgreSQL + pgAdmin

```bash
cd databases/sql/postgresql
docker-compose up -d
````

Access pgAdmin at: [http://localhost:8080](http://localhost:8080)

### Redis + Redis Commander

```bash
cd databases/nosql/redis
docker-compose up -d
```

Access Redis Commander at: [http://localhost:8081](http://localhost:8081)

---

### qDrant vector database

```bash
cd databases/vector/qdrant
docker-compose up -d
```

## 🧹 Cleanup

To remove containers and volumes:

```bash
docker-compose down -v
```

Run the command within each respective directory (`sql/postgresql` or `nosql/redis`).

---

## 📄 License

This project is licensed under the terms specified in the [LICENSE](./LICENSE) file.
