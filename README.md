# Library App
This project was created with [Microsoft's Accelerate app development guidance using GitHub Copilot tools](https://learn.microsoft.com/en-us/training/modules/guided-project-accelerate-app-development-using-github-copilot-tools).
## Description
Library App is a console-based library management system. It allows users to search for patrons, view patron details, manage loans, and renew memberships. The application uses JSON files for data storage and follows a clean architecture with a focus on testability.

## Project Structure
- `AccelerateDevGitHubCopilot.sln`
- `README.md`
- `src/`
  - `Library.ApplicationCore/`
    - `Entities/`
    - `Enums/`
    - `Interfaces/`
    - `Services/`
    - `Library.ApplicationCore.csproj`
  - `Library.Console/`
    - `appSettings.json`
    - `CommonActions.cs`
    - `ConsoleApp.cs`
    - `ConsoleState.cs`
    - `Json/`
    - `Library.Console.csproj`
    - `Program.cs`
  - `Library.Infrastructure/`
    - `Data/`
    - `Library.Infrastructure.csproj`
- `tests/`
  - `UnitTests/`
    - `ApplicationCore/`
    - `UnitTests.csproj`

## Key Classes and Interfaces
- **ConsoleApp** ([ConsoleApp.cs](src/Library.Console/ConsoleApp.cs))
  - Manages the console-based user interface and handles various states of the application.
- **JsonData** ([JsonData.cs](src/Library.Infrastructure/Data/JsonData.cs))
  - Utility class for loading and saving data from/to JSON files.
- **JsonPatronRepository** ([JsonPatronRepository.cs](src/Library.Infrastructure/Data/JsonPatronRepository.cs))
  - Implements `IPatronRepository` to interact with patron data.
- **JsonLoanRepository** ([JsonLoanRepository.cs](src/Library.Infrastructure/Data/JsonLoanRepository.cs))
  - Implements `ILoanRepository` to interact with loan data.
- **LoanService** ([LoanService.cs](src/Library.ApplicationCore/Services/LoanService.cs))
  - Provides services for managing loans.
- **CommonActions** ([CommonActions.cs](src/Library.Console/CommonActions.cs))
  - Enum representing common actions in the console application.

## Usage
1. Clone the repository.
2. Open the solution file `AccelerateDevGitHubCopilot.sln` in Visual Studio.
3. Build the solution.
4. Run the console application by executing the `Library.Console` project.

## License
This project is licensed under the MIT License.
