# Accord Template Playground - Transaction Execution Panel MVP

## Overview

This prototype introduces the **Transaction Execution Panel** to the Accord Template Playground. It is designed to show that template logic can be implemented, currently featuring a hardcoded example of a money overdue penalty calculation.

## Key Features

1. **Transaction Execution Panel**: A new UI component located at `src/components/TransactionExecutionPanel.tsx` that provides an interface for users to enter transaction data and trigger template logic execution.
2. **In-Browser Execution Simulation**: Demonstrates an execution flow within the browser using a hardcoded example, without relying on an external backend execution environment.
3. **State Management Integration**: Integrated seamlessly with the existing global application state (`src/store/store.ts`), as well as editor panels for a cohesive developer experience.
## Local Setup

To run the MVP on your local machine, follow these steps:

1. Ensure you have **Node.js** (version 18 or higher) installed.
2. Open your terminal, navigate to the project directory, and install the dependencies:
   ```bash
   npm install
   ```
3. Start the local development server:
   ```bash
   npm run dev
   ```
4. Open your web browser and navigate to the localhost URL provided in your terminal (typically `http://localhost:5173`).

## Usage

1. Open the Playground in your browser.
2. The execution panel demonstrates the flow using a hardcoded money overdue logic example.
3. Input the required transaction payload or details (e.g., for the late penalty).
4. Execute the transaction to view the generated state, output, or errors for the hardcoded example.

## Tech Stack

- React
- TypeScript
- Vite
- Zustand (Standard pattern in Accord playground)
- Tailwind CSS

## Next Steps / Future Work

- **Integrate `template-engine` runtime:** Transition from the current lightweight in-browser execution layer (used for MVP UI flow demonstration) to the actual Accord execution model.
- **Mimic `apap` server execution flow:** Follow a similar execution flow to the `apap` server by constructing valid runtime model instances (`Request` and `State`).
- **Structured Outputs:** Pass the `Request` and `State` to the `template-engine` (running in the browser via webpack/Vite) for execution, and display the resulting `Response`, updated `State`, and any `Obligations` in the UI.
- **End-to-End Workflow:** Allow users to edit the template logic, provide `Request` and `State` JSON, run the logic through the `template-engine`, and directly view all structured outputs.
