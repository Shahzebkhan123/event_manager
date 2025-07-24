# Event Manager API – QA Onboarding Assignment

This repo is for my onboarding assignment as a Software QA Analyst/Developer. The goal was to improve and test a FastAPI-based REST API that supports user registration, authentication, and profile management. I had to work through 5 known issues and fix the one shown in the instructor’s video.

I used Docker to run everything, Swagger UI for testing endpoints, PGAdmin for managing the database, and pytest to run and write tests.

---

## ✅ Pull Requests for Fixed Issues

These are the five issues I worked on and submitted pull requests for:

1. **[#267 – Fix: Username validation allows special characters (#1)](https://github.com/Shahzebkhan123/event_manager/pull/267)**  
   Allowed hyphens and underscores in usernames. Fixed pattern validation.

2. **[#268 – Fix password validation: require strong passwords (#2)](https://github.com/Shahzebkhan123/event_manager/pull/268)**  
   Enforced stricter password rules: 8+ chars, uppercase, lowercase, number, and special symbol.

3. **[#269 – Fix: Profile update edge cases handled correctly (#3)](https://github.com/Shahzebkhan123/event_manager/pull/269)**  
   This one matches the instructor video issue. I made sure bio and profile picture updates work individually and together.

4. **[#270 – Fix: Ensure user role defaults correctly on registration (#4)](https://github.com/Shahzebkhan123/event_manager/pull/270)**  
   The default user role is now set properly during user creation—no more None or missing values.

5. **[#271 – Fix: Add professional onboarding fields (#5)](https://github.com/Shahzebkhan123/event_manager/pull/271)**  
   Added the `is_professional` field to user creation and updates so it’s synced across schemas.

---

## 🔬 Testing and Coverage

I ran all the tests using `pytest`, and everything passed. I also checked Swagger (`http://localhost/docs`) to manually test various user scenarios—creating, updating, etc. Test coverage was already decent, but I focused on writing or adjusting tests specifically for the five issues I fixed.

---

## 🐳 Docker Setup

I ran everything using Docker Compose as shown in the instructor video.  
- Swagger Docs: http://localhost/docs  
- PGAdmin: http://localhost:5050  
- API: FastAPI  
- DB: PostgreSQL

---

## 💭 Reflection

Honestly, this assignment gave me a solid workout. The biggest learning curve was understanding how Pydantic validation works across different schemas and making sure those changes show up correctly in Swagger. Writing custom validations—especially for passwords—was frustrating at first, but it made me more confident with `Field()` and `validator()` use.

Also, working with GitHub like this (issues, pull requests, branches, etc.) felt more real-world than most school projects. It made me understand why clean commits and detailed PRs matter in a team setting. I now know how to catch edge cases better and test smarter.

All in all, this was a good deep dive into building and testing APIs.

---

