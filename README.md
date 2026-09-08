# HexCoded — AI Show Studio Landing Page & Sales Agent

[![Framework](https://img.shields.io/badge/Framework-Next.js%2014-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![Styling](https://img.shields.io/badge/Styling-Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss)](https://tailwindcss.com/)
[![Scheduling](https://img.shields.io/badge/Scheduling-Cal.com-292929?style=flat-square&logo=cal.com)](https://cal.com/)
[![Deployment](https://img.shields.io/badge/Deployment-Vercel-000000?style=flat-square&logo=vercel)](https://vercel.com/)

A production-ready, high-converting landing page built for **HexCoded** — an AI studio that produces full vertical series, short dramas, and short films for commissioned apps (Kuku TV, STAGE, ReelShort) and content teams.

This platform features a dark-themed UI, an embedded AI sales assistant with strict knowledge guardrails, and an automated Cal.com booking modal to schedule client demos.

---

## 🌟 Key Features

- **High-Converting Hero & UI:** Dark-mode design built with Next.js & Tailwind CSS highlighting HexCoded's core value proposition (*"Models make shots, HexCoded makes shows"*).
- **Strictly Grounded AI Sales Agent:** Integrated Chatbase chatbot trained exclusively on HexCoded context.
  - **No Pricing Quotes:** Redirects pricing queries to a live demo call.
  - **Competitor Differentiation:** Positions HexCoded against tools like Magnific, OpenArt, ImagineArt, and LTX Studio by emphasizing 40+ episode character consistency.
- **Automated Cal.com Booking:** Native `@calcom/embed-react` modal integration for instant demo calendar invites and automated confirmation emails.
- **Fully Responsive:** Optimized for desktop, mobile, and webview apps.

---

## 🛠️ Tech Stack

- **Frontend:** [Next.js 14](https://nextjs.org/) (App Router), React, TypeScript
- **Styling:** [Tailwind CSS](https://tailwindcss.com/)
- **AI Agent Integration:** [Chatbase](https://www.chatbase.co/)
- **Scheduling Infrastructure:** [Cal.com](https://cal.com/) (`@calcom/embed-react`)
- **Hosting:** [Vercel](https://vercel.com/)

---

## 🚀 Quick Start

### Prerequisites

Ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v18.0.0 or higher)
- `npm`, `pnpm`, or `yarn`

### Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/rupesh-dhamdhere/Hex-coded.git
   cd Hex-coded
   ```

2. **Install dependencies:**
   ```bash
   # npm
   npm install

   # or pnpm
   # pnpm install

   # or yarn
   # yarn
   ```

3. **Environment variables** (example):
   - Create a `.env.local` at the project root and add the keys your app expects. Example variables:
     ```env
     NEXT_PUBLIC_CHATBASE_API_KEY=your_chatbase_api_key
     NEXT_PUBLIC_CALCOM_URL=your_calcom_public_embed_url
     # Any other API keys or feature flags
     ```
   - Never commit secrets to the repository.

4. **Run the development server:**
   ```bash
   npm run dev
   # or
   pnpm dev
   # or
   yarn dev
   ```

5. **Build for production:**
   ```bash
   npm run build
   npm run start
   ```

---

## Usage & Integration Notes

- Chatbase: The AI sales agent is intentionally grounded only on HexCoded content. Configure your Chatbase bot (or equivalent) so it refuses pricing and competitor pricing queries and instead directs users to schedule a demo via the Cal.com modal.
- Cal.com: Use `@calcom/embed-react` to show an in-page booking modal. Keep the booking flow simple (15/30/45 minute demo options) and ensure confirmation emails include links to a prepared demo deck.
- Accessibility: Follow semantic HTML, provide ARIA labels for interactive widgets (chat, booking), and test the dark theme for sufficient contrast.

---

## Deployment

- Recommended: Deploy to [Vercel](https://vercel.com/) for seamless Next.js support and edge network performance.
- Configure environment variables in your Vercel project dashboard (do not expose secret keys in client-side variables unless required and safe).

---

## Testing

- Unit & integration tests: Add your preferred test runner (Jest, Vitest, React Testing Library).
- E2E: Consider Playwright or Cypress for full flow tests (chat + booking modal).

```bash
# Example test commands
npm test
# or
npm run test:e2e
```

---

## Contributing

Contributions are welcome. Please open an issue to discuss major changes before submitting a pull request.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add feature"`)
4. Push to your branch and open a Pull Request

Please follow the repository's code style and include tests for new behavior.
