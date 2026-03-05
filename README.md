# LNote

A full-stack notes and knowledge-sharing platform with user authentication, categories, collections, comments, real-time messaging, and full-text search.

## Tech Stack

### Backend

| Category      | Technology                    |
|---------------|-------------------------------|
| Framework     | Spring Boot 2.7.18            |
| Security      | Spring Security              |
| Persistence   | MyBatis                       |
| Database      | MySQL 8.0                     |
| Cache         | Redis                         |
| Messaging     | WebSocket                     |
| Search        | MySQL full-text + Jieba       |
| Storage       | Local filesystem              |
| Logging       | Log4j2                        |
| Markdown      | Flexmark                      |
| Email         | Spring Mail                   |
| Templating    | Thymeleaf                     |
| Utilities     | Hutool                        |
| Testing       | JUnit                         |

### Frontend

| Category      | Technology                    |
|---------------|-------------------------------|
| Build        | Vite                          |
| Framework    | React 18 + TypeScript         |
| Routing      | React Router DOM              |
| State        | Redux Toolkit                 |
| UI           | Ant Design                    |
| Styling      | TailwindCSS                   |
| HTTP         | Axios                         |
| Markdown     | Cherry Markdown               |
| Quality      | ESLint, Prettier              |
| Git hooks    | Husky, lint-staged            |

### Development

- **IDE:** Any (e.g. IntelliJ IDEA 2024+, VS Code)
- **JDK:** 17
- **Node:** 18+
- **Package manager:** Maven (backend), npm/pnpm (frontend)
- **Version control:** Git

## Project Structure

```
LNote/
├── backend/          # Spring Boot API
│   ├── src/
│   └── pom.xml
├── frontend/         # React SPA
│   ├── src/
│   └── package.json
└── README.md
```

## Prerequisites

- JDK 17
- Maven 3.6+
- Node.js 18+
- MySQL 8.0
- Redis

## Getting Started

### Backend

1. Create a MySQL database and configure `application.yml` (or env) with URL, username, and password.
2. Ensure Redis is running and reachable.
3. From the project root:

```bash
cd backend
./mvnw spring-boot:run
```

The API runs by default on the port defined in your Spring Boot config (e.g. `8080`).

### Frontend

1. Install dependencies:

```bash
cd frontend
npm install
```

2. Set environment variables (e.g. in `.env` or `.env.development`) for the API base URL.
3. Start the dev server:

```bash
npm run dev
```

4. Build for production:

```bash
npm run build
```

### Docker (optional)

If a `Dockerfile` or `docker-compose.yml` is provided in the repo, you can run the backend (and optionally frontend) via Docker. Refer to those files for exact commands.

## Scripts

### Backend

- `./mvnw spring-boot:run` — run the application
- `./mvnw test` — run tests
- `./mvnw package` — build JAR

### Frontend

- `npm run dev` — start Vite dev server
- `npm run build` — TypeScript check + production build
- `npm run preview` — preview production build
- `npm run lint` — run ESLint
- `npm run format` — format with Prettier
- `npm run format:check` — check formatting

## Configuration

- **Backend:** Use `application.yml` / `application.properties` and environment variables for datasource, Redis, JWT, file paths, and mail settings.
- **Frontend:** Use `.env`, `.env.development`, and `.env.production` for API base URL and other env-specific values.

## License

See [LICENSE](LICENSE) in the repository root.
