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

## Styling

Uses custom CSS utility classes (Tailwind-like) in `wwwroot/css/app.css`:
- Layout: `.flex`, `.grid`, `.items-center`
- Spacing: `.p-4`, `.mb-2`, `.mx-auto`
- Colors: `.bg-accent`, `.bg-marked`, `.text-gray-700`

## State Management

- `BingoGameService` manages game state with event-driven updates
- State persisted to localStorage via JSInterop
- Components subscribe to `OnStateChanged` event

## Design Guide

To maintain a cohesive and minimalistic design throughout the project, follow these guidelines:

### Typography
- Use `IBM Plex Sans` as the primary font for all text.
- Ensure consistent font sizes and weights for headings, body text, and buttons.

### Color Palette
- Stick to the defined monochromatic palette:
  - Background: `#ffffff` (light) or `#000000` (dark mode).
  - Accent Color: `#0078d4`.
  - Text: `#333333` (primary), `#666666` (secondary).

### Layout and Spacing
- Use consistent spacing units (e.g., `1rem`, `2rem`) for padding and margins.
- Align content to a grid or flexbox layout for clean and structured designs.

### Components
- Buttons:
  - Primary buttons should use the accent color with white text.
  - Add hover effects for better interactivity.
- Cards and Panels:
  - Use subtle shadows or borders to differentiate sections.

### Animations
- Keep animations subtle and purposeful (e.g., hover effects, page transitions).
- Avoid excessive or distracting animations.

### Accessibility
- Ensure sufficient color contrast for text and interactive elements.
- Test designs with screen readers and keyboard navigation.
