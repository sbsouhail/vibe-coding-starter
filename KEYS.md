# Your free Gemini API key

Inside Google AI Studio, your app's AI works with no setup. As soon as you run your app **anywhere else** (on your laptop, in Bolt, in Cursor, or on a hosting service), you need your own key. It's free.

## 1. Get a free key (2 minutes)

1. Go to [aistudio.google.com](https://aistudio.google.com) and sign in with your personal Gmail.
2. Click **Get API key**, then **Create API key**.
3. Copy the key. Treat it like a password.

The free tier needs no credit card. It has rate limits per minute and per day, and not every model is available on it. Check your current limits on the [rate limit page](https://aistudio.google.com/rate-limit).

## 2. Use it in your app

Apps exported from AI Studio read the key from an environment variable called `GEMINI_API_KEY`.

**On your laptop:**

1. Copy `.env.example` to a new file named `.env`.
2. Replace the placeholder with your key:
   ```
   GEMINI_API_KEY="paste-your-key-here"
   ```
3. Run `npm install`, then `npm run dev`.

**In Bolt, Lovable or a hosting service:** open the project's settings, find **Secrets** or **Environment variables**, and add `GEMINI_API_KEY` with your key.

## 3. Keep it safe

- **Never commit `.env` to GitHub.** Check that `.env` is listed in your `.gitignore` file. Only `.env.example`, with a fake value, belongs in the repo.
- **Never put the key in frontend code.** Anyone visiting your site could copy it. Keep AI calls on the server side, as AI Studio does.
- **Leaked a key by mistake?** Delete it in AI Studio and create a new one right away.

## 4. Good to know

- **Limits are per project, not per key.** Creating more keys in the same project doesn't give you more quota. Each teammate can create their own key on their own account, which has its own quota.
- **Daily limits reset at midnight Pacific time**, which is 9:00 in Tunisia.
- **Free-tier data may be used by Google to improve its products.** Don't send personal or sensitive data through the free tier.
- **Getting a `403 PERMISSION_DENIED` error?** Your account may need age verification, or the model you chose isn't available on the free tier. Check the rate limit page and try a different model.

Sources: [Gemini API rate limits](https://ai.google.dev/gemini-api/docs/rate-limits) · [Gemini API billing](https://ai.google.dev/gemini-api/docs/billing) · [AI Studio Build mode](https://ai.google.dev/gemini-api/docs/aistudio-build-mode)
