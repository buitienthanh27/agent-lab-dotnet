# Copilot Workspace Instructions

## Development Checklist

Before committing any changes, ensure:

- [ ] `dotnet build` passes with no errors
- [ ] `dotnet test` passes (when tests exist)
- [ ] Code follows C# conventions (PascalCase for public members)
- [ ] No unused variables or imports

## Project Overview

**Soc Ops** is a Social Bingo game built with Blazor WebAssembly (.NET 10). Players find people who match questions to mark squares and get 5 in a row.

## Architecture

```
SocOps/
├── Components/     # Reusable Blazor components
│   ├── BingoBoard.razor
│   ├── BingoSquare.razor
│   ├── BingoModal.razor
│   ├── GameScreen.razor
│   └── StartScreen.razor
├── Models/         # Data models (BingoSquareData, GameState)
├── Services/       # Business logic
│   ├── BingoGameService.cs    # State management
│   └── BingoLogicService.cs   # Game logic
├── Data/           # Static data (Questions.cs)
├── Pages/          # Routable pages (Home.razor)
└── wwwroot/        # Static assets & CSS
```

## Key Commands

```bash
dotnet build SocOps/SocOps.csproj  # Build
dotnet run --project SocOps       # Run dev server (port 5166)
dotnet test                        # Run tests
```

## Contribution Guidelines

1. **Fork the Repository**:
   - Create a personal copy of the repository on GitHub.

2. **Create a Feature Branch**:
   - Use a descriptive name for your branch:
     ```bash
     git checkout -b feature/your-feature-name
     ```

3. **Make Changes**:
   - Implement your changes and ensure they follow the development checklist.

4. **Commit Changes**:
   - Write clear and concise commit messages:
     ```bash
     git commit -m "Add feature description"
     ```

5. **Push Changes**:
   - Push your branch to GitHub:
     ```bash
     git push origin feature/your-feature-name
     ```

6. **Create a Pull Request**:
   - Open a pull request on GitHub and describe your changes.

---