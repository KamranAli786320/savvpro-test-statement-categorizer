
# AI Usage Disclosure

## 1. AI Tools Used

- **Tool:** ChatGPT
- **Purpose:** Learning support, code suggestions, debugging assistance, test-writing guidance, and documentation drafting.
- **Human responsibility:** I reviewed the suggested implementation, ran the application locally, executed tests, and checked the results.

## 2. How AI Assisted

ChatGPT helped me work through the project in small, understandable steps. I used it to:

- Understand the assessment requirements and plan the application structure.
- Develop a Python/FastAPI backend for CSV upload and validation.
- Build a transparent, keyword-based transaction categorization engine.
- Create backend tests for categorization rules and API validation.
- Develop a React and TypeScript interface for uploading transactions, reviewing categories, correcting results, and exporting CSV.
- Troubleshoot CSV parsing issues and understand test failures.
- Draft the README and design documentation.

## 3. Where AI Suggestions Needed Verification

AI-generated suggestions were not treated as automatically correct. I checked the implementation by running the application and tests.

- CSV files can contain leading blank lines or unexpected headers. I tested and corrected a sample CSV parsing issue.
- A keyword-based engine cannot confidently recognize every merchant or transaction description. Unknown transactions are therefore marked `Needs Review`.
- Refund and transfer rules depend on the available description text. They cannot guarantee that every refund or transfer will be recognized.
- The frontend currently keeps reviewed changes in application state. The user must export the results to retain those changes outside the current session.

These limitations are documented so that users understand where manual review is necessary.

## 4. Human Verification

I ran the backend test suite locally. At the time of recording this disclosure, all eight tests passed:

- Four categorization tests.
- Four API tests covering the home endpoint, valid CSV upload, unsupported file type, and missing required columns.

I also tested uploading synthetic sample transactions through the local application and checked that the returned categories were displayed.

Test results should be rerun before final submission if the code changes.

## 5. Token Usage and Evidence

I used ChatGPT for interactive development assistance. An exact token count for this conversation is not available to me in the information shown by the chat interface, so I have not invented a token total.

Evidence to include with this submission:
- A screenshot of the relevant ChatGPT conversation showing the development assistance used.
- A screenshot of the successful local test run.
- Any available tool usage or token report, if the tool provides one.

Screenshots should not contain passwords, API keys, personal information, or real financial records.

## 6. Data and Privacy

The sample transactions used for development are synthetic. No real bank statement or financial account credentials should be committed to this repository.

## 7. Final Note

AI was used as a development and learning assistant. The transaction categorization decision engine itself uses explicit Python rules and does not delegate transaction classification to a large language model.
