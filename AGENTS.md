# Project Security & Development Guidelines

1. **API Keys & Credentials**:
   - Never hardcode private keys, service account secrets, or admin credentials in source code.
   - Use standard client SDKs for the web frontend, and proxy sensitive admin operations through secure server endpoints or security rules.

2. **Environment & Secrets Handling**:
   - Maintain `.env.example` to document expected environment variables.
   - Maintain a complete `.gitignore` file preventing sensitive credential files (e.g. `.env`, `*.pem`, `serviceAccountKey.json`, `firebase-adminsdk*.json`) from being tracked.

3. **Firebase Security Rules**:
   - Always write structured, attribute-validating Firebase Security Rules in `firestore.rules`.
   - Avoid unrestricted wildcard rules (`allow read, write: if true;`).
