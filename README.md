# README.md

## LKS Cloud Computing DIY 2024

### Prerequisites
- Docker
- Docker Compose
- AWS S3 Credentials

### Environment Variables
Create a `.env` file and configure the following environment variables:
```env
DB_USER=yourdbuser
DB_PASS=somethingsecret
DB_HOST=db
DB_PORT=3306
DB_NAME=student_db

REDIS_ADDR=redis:6379

AWS_REGION=us-east-1
AWS_ACCESS_KEY=your_access_key
AWS_SECRET_KEY=your_secret_key
AWS_BUCKET_NAME=your_bucket_name
```

### How to Run with Docker
1. Build and run the container:
   ```sh
   docker-compose up --build -d
   ```
2. The API will be available at `http://YOUR_IP_ADDRESS:8080`

### API Endpoints
| Method | Endpoint               | Description              |
|--------|------------------------|--------------------------|
| POST   | `/students`            | Create a student        |
| GET    | `/students`            | Get all students        |
| GET    | `/students/:id`        | Get student by ID       |
| PUT    | `/students/:id`        | Update student          |
| DELETE | `/students/:id`        | Delete student          |
| GET    | `/students/cache/:id`  | Get student from cache  |

3. Stop the container:
   ```sh
   docker-compose down
   ```
---