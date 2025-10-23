# Cs635-refactoring-project
# OpenBoxes Stock Movement Refactor – Ivy Huynh

This is a small, self-contained Groovy/Gradle project that models a portion of the OpenBoxes Stock Movement workflow.
I built this sandbox to demonstrate a clean, modular refactoring plan focused on separation of concerns, testability, and maintainable design.
# Refactoring Highlights
Introduced an Orchestrator and Repository boundary to separate workflow control from data access
Implemented a clear State Machine for stock movement status transitions
Added Ports and Adapters to handle external dependencies (time, inventory, label parsing)
Defined Pure Policy Classes (e.g., AllocationPolicy) to encapsulate business rules with fast unit tests (Spock)
# Quick Start
Install Java 17 and Gradle (or use ./gradlew if you add a wrapper).
From the project root, run:
gradle test
All tests should pass successfully.

You can modify the orchestrator, policies, or create new tests to explore additional refactoring improvements.
Project Structure
core/ – Domain value objects and state machine logic
ports/ – Interfaces for connecting to external systems
policy/ – Business rules and allocation strategies
app/ – Orchestrator, repository interfaces, and adapters
domain/ – Minimal placeholder entities modeled after OpenBoxes objects
Notes
This project is not the official OpenBoxes codebase.
It is a clean-room sandbox designed for educational purposes to demonstrate refactoring principles applied to the Stock Movement workflow.
