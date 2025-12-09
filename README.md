
# Ahorrista – React + TypeScript Hackathon (2h)

Frontend SPA built in **2 hours** for the “Ahorrista” hackathon.  
The app helps young Peruvians visualize and control their personal expenses, consuming an existing REST API efficiently with **React + TypeScript**.

---

## 1. What the app does

- 🔐 **Auth with JWT**
  - Register and login against `/authentication/register` and `/authentication/login`
  - Stores the JWT and sends it as `Authorization: Bearer <token>` in protected calls

- 💰 **Expenses**
  - Shows **monthly expense summary by category** (from `/expenses_summary`)
  - Loads **detailed expenses only when the user clicks a category**  
    → efficient API usage for +10,000 expenses/user (`/expenses/detail`)
  - Allows creating and deleting expenses (`POST /expenses`, `DELETE /expenses/:id`)
  - Uses `/expenses_category` to list categories

- 🎯 **Savings goals**
  - List, create and update monthly goals via `/goals` (GET/POST/PATCH)

---

## 2. Key implementation points

- **Single Page Application (SPA)** with React + TypeScript
- **API consumption principle**:
  - First load: only monthly summary
  - On click: load detail for that category/month
- **State management** with React hooks (and simple lifting of state between components)
- **UI/UX** focused on:
  - Clear login/register flow
  - Dashboard with monthly summary and category cards
  - Detail view with list of expenses and actions
  - Simple section for viewing and editing goals

---

## 3. Tech stack

- React
- TypeScript
- Fetch/axios for REST calls
- JWT handling on the client (token storage + header injection)

---

## 4. Notes

- Built under a **strict 2-hour time limit** in a small 3-team.
- Focused on:
  - Correct JWT flow
  - Efficient API usage (lazy loading of details)
  - Clean component structure and basic TypeScript typing.
