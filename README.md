# 📚 BookStoreValidation API

## 🚀 Tech Stack

- ASP.NET Core 8.0
- C#
- Entity Framework Core (Code-First)
- FluentValidation
- AutoMapper
- Swagger 
- RESTful API principles

---

## ✅ Validation

This project uses [FluentValidation](https://docs.fluentvalidation.net/en/latest/) to validate incoming data before executing business logic. Validation rules are applied in command classes for cleaner and maintainable code.

### Validation Rules

#### 📘 CreateBookCommandValidator

- `Title`: Must not be empty and must have a minimum length of 4 characters.
- `GenreId`: Must be greater than 0.
- `PageCount`: Must be greater than 0.
- `PublishDate`: Must not be default `DateTime`.

#### 📝 UpdateBookCommandValidator

- `BookId`: Must be greater than 0.
- `Title`: Must not be empty and must have a minimum length of 4 characters.
- `GenreId`: Must be greater than 0.

#### ❌ DeleteBookCommandValidator

- `BookId`: Must be greater than 0.

### Example

If an invalid request is made (e.g., title is empty or ID is 0), the API will return a `400 Bad Request` with a meaningful validation error message.




