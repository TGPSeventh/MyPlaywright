# MyPlaywright

This project uses **Playwright** with **TypeScript** for browser automation. It is designed to be developed and run inside **Google Cloud Shell Editor**.

---

## 📚 Table of Contents

- [Project Structure](#-project-structure)
- [Getting Started in Google Cloud Shell](#-getting-started-in-google-cloud-shell)
  - [Clone the Repo](#1-clone-the-repo)
  - [Initialize Node Project](#2-initialize-node-project)
  - [Install Dependencies](#3-install-dependencies)
- [Setting up Playwright](#-setting-up-playwright)
  - [Option 1: Scaffold Automatically](#option-1-scaffold-automatically)
  - [Option 2: Manual Setup](#option-2-manual-setup)
    - [Create `playwright.config.ts`](#create-playwrightconfigts)
    - [Create `tsconfig.json`](#create-tsconfigjson)
    - [Add a Sample Test](#add-a-sample-test)
- [Running Tests](#-running-tests)
- [Running Test with Specific File](#-running-test-with-specific-file)
- [Helpful Commands](#-helpful-commands)
- [Resources](#-resources)
- [Git Setup](#-git-setup)
  - [Initialize](#initialize)
  - [Connect to Git](#connect-to-git)

## 📁 Project Structure

## 🚀 Getting Started in Google Cloud Shell

### 1. Clone the Repo
git clone https://github.com/TGPSeventh/MyPlaywright.git
cd MyPlaywright

### 2. Initialize Node Project
npm init -y

### 3. Install Dependencies
npm install

## 🔧 Setting up Playwright

### Option 1: Scaffold Automatically
npx create-playwright@latest

### Option 2: Manual Setup

#### Create `playwright.config.ts`
    # import { defineConfig } from '@playwright/test';
    # export default defineConfig({
    #   testDir: './tests',
    #   use: {
    #     headless: true,
    #     viewport: { width: 1280, height: 720 },
    #     baseURL: 'https://example.com',
    #   },
    # });
#### Create `tsconfig.json`
    # {
    #   "compilerOptions": {
    #     "target": "ESNext",
    #     "module": "CommonJS",
    #     "moduleResolution": "Node",
    #     "strict": true,
    #     "esModuleInterop": true,
    #     "skipLibCheck": true,
    #     "forceConsistentCasingInFileNames": true,
    #     "outDir": "dist"
    #   },
    #   "include": ["tests/**/*.ts", "lib/**/*.ts"]
    # }
#### Add a Sample Test
    # import { test, expect } from '@playwright/test';

    # test('homepage has title', async ({ page }) => {
    #   await page.goto('https://playwright.dev');
    #   await expect(page).toHaveTitle(/Playwright/);
    # });

## 🏃 Running Tests
npx playwright test

## 🏃 Running Test with Specific File
npx playwright test tests/example.spec.ts

## 🧪 Helpful Commands
# Install browsers:
    npx playwright install

    ### headful mode ###
    npx playwright test --headed

    ### Test with a UI (optional) ###
    npx playwright test --ui

    # Open test report:
    npx playwright show-report

    # Record test steps:
    npx playwright codegen https://example.com

## 🔗 Resources
    Playwright Docs
    TypeScript Docs

## 🖥️ Git Setup

### Initialize
    # git init
    # git add .
    # git commit -m "Initial commit"
### Connect to Git
    #git remote add origin https://github.com/your-username/your-repo.git
    #git branch -M main
    #git push -u origin main