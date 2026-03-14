# Copilot Workspace Instructions

## Checklist

Before committing changes:
- [ ] `dotnet build` passes
- [ ] `dotnet test` passes
- [ ] Code follows C# conventions

## Overview

**Soc Ops**: A Social Bingo game built with Blazor WebAssembly (.NET 10).

## Architecture

```
SocOps/
├── Components/     # Blazor components
├── Models/         # Data models
├── Services/       # Business logic
├── Data/           # Static data
├── Pages/          # Routable pages
└── wwwroot/        # Static assets
```

## Commands

```bash
dotnet build SocOps/SocOps.csproj  # Build
dotnet run --project SocOps       # Run dev server
dotnet test                        # Run tests
```

## Contribution

1. **Fork & Branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```
2. **Commit**:
   ```bash
   git commit -m "Add feature"
   ```
3. **Push & PR**:
   ```bash
   git push origin feature/your-feature-name
   ```