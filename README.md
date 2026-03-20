# Accord Template Playground - Transaction Execution MVP

## Overview

This MVP introduces the **Transaction Execution Panel** to the Accord Template Playground. It allows users to execute TypeScript template logic directly within the playground environment using a custom in-browser execution mechanism.

## Key Features

1. **Transaction Execution Panel**: A new UI component located at `src/components/TransactionExecutionPanel.tsx` that provides an interface for users to enter transaction data and trigger template logic execution.
2. **In-Browser Execution Service**: Evaluates and executes TypeScript template logic securely and efficiently within the browser itself without relying on an external backend execution environment.
3. **State Management Integration**: Integrated seamlessly with the existing global application state (`src/store/store.ts`), as well as editor panels for a cohesive developer experience.

## Usage

1. Open the Playground in your browser.
2. The execution panel allows interacting dynamically with your template logic.
3. Input the required transaction payload or details.
4. Execute the transaction to view the generated state, output, or errors.

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
