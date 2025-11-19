# Library App

## Description

Library App is a Python-based application for managing library patrons, books, loans, and related operations. It provides a console interface for searching patrons, viewing loan details, renewing memberships, and managing book loans. The project demonstrates clean architecture principles, using entities, services, repositories, and interfaces for extensibility and maintainability.

## Project Structure

- AZ2007LabAppM2Python/
    - AccelerateDevGHCopilot/
        - README.md
        - library/
            - application_core/
                - entities/
                    - author.py
                    - book.py
                    - book_item.py
                    - loan.py
                    - patron.py
                - enums/
                    - loan_extension_status.py
                    - loan_return_status.py
                    - membership_renewal_status.py
                - interfaces/
                    - iloan_repository.py
                    - iloan_service.py
                    - ipatron_repository.py
                    - ipatron_service.py
                - services/
                    - loan_service.py
                    - patron_service.py
            - console/
                - common_actions.py
                - console_app.py
                - console_state.py
                - main.py
            - infrastructure/
                - json_data.py
                - json_loan_repository.py
                - json_patron_repository.py
                - Json/
                    - Authors.json
                    - Books.json
                    - BookItems.json
                    - Loans.json
                    - Patrons.json
            - tests/
                - test_loan_service.py
                - test_patron_service.py

## Key Classes and Interfaces

- **Entities**
    - `Author`: Represents a book author.
    - `Book`: Represents a book with metadata and author.
    - `BookItem`: Represents a physical copy of a book.
    - `Loan`: Represents a book loan transaction.
    - `Patron`: Represents a library user.

- **Enums**
    - `LoanExtensionStatus`: Status codes for loan extension.
    - `LoanReturnStatus`: Status codes for returning a loan.
    - `MembershipRenewalStatus`: Status codes for membership renewal.

- **Interfaces**
    - `ILoanRepository`: Abstracts loan data access.
    - `ILoanService`: Abstracts loan-related business logic.
    - `IPatronRepository`: Abstracts patron data access.
    - `IPatronService`: Abstracts patron-related business logic.

- **Services**
    - `LoanService`: Implements loan management logic.
    - `PatronService`: Implements patron membership logic.

- **Infrastructure**
    - `JsonData`: Loads and saves data from JSON files.
    - `JsonLoanRepository`: Loan repository backed by JSON.
    - `JsonPatronRepository`: Patron repository backed by JSON.

- **Console**
    - `ConsoleApp`: Main console application loop.
    - `ConsoleState`: Enum for console states.
    - `CommonActions`: Enum for common user actions.

## Usage

1. **Setup**
    - Ensure Python 3.12+ is installed.
    - Install dependencies if required.

2. **Run the Application**
    - Navigate to the `library/console` directory.
    - Execute:
      ```sh
      python3 main.py
      ```
    - Follow the console prompts to search patrons, view loans, renew memberships, and manage book loans.

3. **Run Tests**
    - Navigate to the `library/tests` directory.
    - Execute:
      ```sh
      python3 -m unittest test_loan_service.py
      python3 -m unittest test_patron_service.py
      ```

## License

This project is licensed under the MIT License. See the LICENSE file for details.