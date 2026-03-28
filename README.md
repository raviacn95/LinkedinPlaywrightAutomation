# Naukri Automation

Playwright-based automation for applying to jobs on Naukri with reusable locator healing, saved session support, and configurable default answers for application questions.

## Project Structure

- `tests/naukri-apply.spec.ts`: main automation flow
- `src/healer.ts`: locator fallback and healing helpers
- `config.json`: runtime configuration and default chatbot answers
- `run-naukri-apply.ps1`: PowerShell runner that writes logs under `logs/`

## Prerequisites

- Node.js installed
- NPM installed

## Install

```bash
npm install
```

## Run

Use the direct TypeScript entrypoint:

```bash
npx tsx tests/naukri-apply.spec.ts
```

Or use the PowerShell runner:

```powershell
./run-naukri-apply.ps1
```

## Configuration

Update `config.json` to control:

- total loops
- jobs selected per loop
- target URL
- login timeout
- headless mode
- default answers for Naukri chatbot questions

## Notes

- Session state is stored locally in `naukri-session.json` and is intentionally ignored by Git.
- Logs and debug screenshots are kept out of source control.
