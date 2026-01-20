# Pseudata

**Deterministic mock data generation across all programming languages**

> [!WARNING]
> **Status: Active Development** - No releases yet. Watch this repo to follow progress.

## The Problem

Traditional faker libraries (faker.js, Faker Python, gofakeit) produce different data across languages. Same seed, different results = broken integration tests.

Your frontend expects Alice. Your backend returns Bob.

```python
# Python backend (Faker)
from faker import Faker
fake = Faker()
Faker.seed(123)
print(fake.name())  # → "Brett Davis"
```

```typescript
// TypeScript frontend (faker.js)
import { faker } from "@faker-js/faker";
faker.seed(123);
console.log(faker.person.fullName()); // → "Miss Dora Kiehn"
```

**Same seed. Different data. Integration chaos.**

## The Solution

Pseudata uses a standardized algorithm (PCG32) to generate **identical data across Go, Java, Python, and TypeScript**.

```go
// Go
users := pseudata.NewUserArray(42)
user := users.At(1000)
fmt.Println(user.Name)  // → "John Smith"
```

```java
// Java
UserArray users = new UserArray(42);
User user = users.at(1000);
System.out.println(user.getName()); // → "John Smith"
```

```python
# Python
users = UserArray(42)
user = users.at(1000)
print(user.name)  # → "John Smith"
```

```typescript
// TypeScript
const users = new UserArray(42);
const user = users.at(1000);
console.log(user.name); // → "John Smith"
```

**Same seed. Same index. Same data. Every language.**

## Key Features

- **Cross-Language Consistency** - Same seed = same data across all languages
- **Infinite Scale** - O(1) instant access to billions of records with zero memory overhead
- **Stateless Relations** - Create deterministic relationships without a database. Navigate entities in O(1) time
- **Smart Locale Loading** - Minimal default, scale globally. Load only the specific regions and data you need

## Documentation

**Visit [pseudata.dev](https://pseudata.dev)** for complete documentation:

- [Introduction Blog Post](https://pseudata.dev/blog/introduction/) - Why this matters
- [Get Started Guide](https://pseudata.dev/guides/get-started/) - Quick introduction
- [Technical Concept](https://pseudata.dev/reference/concept/) - Deep dive into architecture
- [RSS Feed](https://pseudata.dev/rss.xml) - Subscribe to updates

## Roadmap

**Phase 1 (Current):** Core Language Support
- Finalize Go, Java, Python, and TypeScript implementations
- Ensure 100% cross-language consistency
- Comprehensive test coverage
- Initial stable release (v1.0)

**Phase 2:** Backend Expansion
- C# for .NET ecosystems
- Rust for high-performance systems
- PHP for web applications

**Phase 3:** Mobile Platforms
- Swift for iOS development
- Dart for Flutter cross-platform apps

**Phase 4:** Advanced Features
- Additional data types (Products, Companies, Financial data)
- Custom schema definitions
- Plugin architecture for domain-specific generators
- Performance optimizations

## Contributing

**Not accepting contributions yet.** We're still finalizing the core architecture and ensuring 100% cross-language consistency.

Once v1.0 releases, we'll welcome:
- Bug reports and feature requests
- Additional language implementations
- Documentation improvements
- Test case contributions

## Current Status

**Active development** with working implementations in:

- Go
- Java
- Python
- TypeScript

The core PCG32 algorithm and virtual array architecture are established. We're now focusing on:
1. Comprehensive test coverage
2. Cross-language validation
3. Documentation and examples
4. Performance benchmarking

## Stay Updated

- **Star this repo** to follow development
- **Subscribe** to the [RSS feed](https://pseudata.dev/rss.xml)
- **[Watch releases](https://github.com/pseudata/pseudata/releases)** to get notified when v1.0 ships

## License

Apache License 2.0

Copyright © 2025 Pseudata Project

