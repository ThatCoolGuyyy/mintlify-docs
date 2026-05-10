# Instructor Documentation Site

A Mintlify documentation site for the [Instructor](https://python.useinstructor.com) Python library. Built as the capstone deliverable for the Hackmamba Technical Writer Course.

## Site structure

| Page | Diataxis type | File |
|---|---|---|
| Overview | Landing | `index.mdx` |
| Getting Started | Tutorial-adjacent | `getting-started.mdx` |
| Extract structured data | Tutorial | `tutorial.mdx` |
| Build a production FastAPI endpoint | How-To | `how-to-fastapi.mdx` |
| API Reference | Reference | `api-reference/*.mdx` |
| Troubleshooting | Reference | `troubleshooting.mdx` |

## Local development

```bash
# Install the Mintlify CLI (requires Node.js v19+)
npm install -g mint

# Preview the site locally
mint dev
```

The site runs at `http://localhost:3000`.

## Deployment

The site deploys automatically to Mintlify when changes land on the `main` branch. To set up deployment:

1. Push this repository to GitHub.
2. Connect the repo in your Mintlify dashboard.
3. Install the Mintlify GitHub App.

Every push to `main` triggers a deployment.

## Linting

Vale runs on every push and pull request via the GitHub Action at `.github/workflows/vale.yml`. The configuration uses the Microsoft Writing Style Guide as the base.

To run Vale locally:

```bash
# Install Vale
brew install vale

# Sync style packages
vale sync

# Lint the docs
vale .
```

## Verification

All code examples are verified against Instructor `1.14.5`. The SSE format used in the FastAPI How-To is verified against the WHATWG HTML living standard.
