# Tech Baseline

The following technologies are the mandated baseline for new and existing projects.

| Category | .NET / C# Standard |
|---|---|
| **.NET SDK** | Use the Long-Term Support (LTS) version of the .NET SDK. |
| **Framework** | ASP.NET Core 8.0 or newer LTS. |
| **Build** | .NET CLI (`dotnet build`) / MSBuild (with SDK-style `.csproj` files). |
| **Dependency Control** | NuGet. Enforce versions centrally using **Directory.Packages.props**. Use private artifact repositories if applicable. |
| **HTTP Client** | `IHttpClientFactory` (for managing `HttpClient` instances) or use Refit. |
| **Persistence (ORM)** | Entity Framework Core 8 LTS or Dapper based on project requirements. |
| **Migrations** | EF Core Migrations, DbUp. |
| **Database** | MS SQL Server, Postgresql (preferred). |
| **Messaging (Transactional/Workflow)** | Use a message broker such as Azure Service Bus or RabbitMQ. Apply MassTransit or similar frameworks for simplified .NET integration. |
| **Messaging (Streaming/Analytics)** | Use Kafka or Azure Event Hub. Use Schema Registry (Azure/Confluent). |
| **Messaging Design** | Always design messages to be idempotent, versioned, and self-contained. Implement dead-letter queues or equivalent handling for failures. |
| **Observability** | **OpenTelemetry for .NET** (built-in standard for metrics and traces). |
| **Logging** | `Microsoft.Extensions.Logging` (`ILogger<T>`) facade with **Serilog** as the provider, configured for JSON output. |
| **Container** | Runtime Image: `mcr.microsoft.com/dotnet/aspnet:8.0-alpine` (preferred) or `mcr.microsoft.com/dotnet/aspnet:8.0`. |