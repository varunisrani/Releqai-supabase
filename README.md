# ReleqAI Supabase

ReleqAI Supabase is a React prototype for browsing, searching, and categorizing AI tools and prompt collections with Supabase-backed authentication and data.

## Core features

- Supabase email/password signup, login, session tracking, and logout flows.
- Auth-gated home view with AI-tool, ReleqAI-tool, and prompt sections.
- Static catalogs of AI tools, categories, and prompts.
- Supabase-backed tool search using case-insensitive matching.
- Text and browser speech-recognition search interfaces.
- Light/dark theme context.
- Contact-form and chat demonstration routes.

## Technology stack

- React 18 and React Router 6
- Vite 5 with the React SWC plugin
- JavaScript/JSX and Tailwind CSS 3
- Supabase JavaScript client and Supabase Auth UI
- Material UI, React Hook Form, Lottie, and React Toastify

## Prerequisites

- Node.js compatible with the locked dependencies
- npm
- Access to a compatible Supabase project for authentication and database-backed views
- A browser with Web Speech API support for voice search

## Local setup

```bash
git clone https://github.com/varunisrani/Releqai-supabase.git
cd Releqai-supabase
npm ci
npm run dev
```

Build and inspect the production bundle with:

```bash
npm run build
npm run preview
```

Lint the project with `npm run lint`.

## Configuration

The current source does not define environment-variable names. Supabase client configuration is embedded directly in client modules and must be reviewed before reuse or deployment. Do not add service-role or other privileged keys to browser code.

## Project structure

- `src/App.jsx` — route definitions and context providers
- `src/Auth/` — login and signup views
- `src/Components/` — catalogs, search, navigation, contact, and chat views
- `src/Components/Arrays/` — static tool, category, and prompt data
- `src/Components/Supabase.js` — primary Supabase client
- `src/Context/` — authentication-session and theme contexts
- `src/Supabase/` — additional Supabase experiments

## Status and limitations

This is an experimental front-end project whose authenticated and database-backed behavior depends on existing Supabase schemas and policies that are not provisioned in this repository. Client configuration is hard-coded in multiple modules; rotate or verify those credentials and migrate configuration before deployment. Voice search is browser-dependent, and several contact/chat routes are demonstrations rather than documented production services.
