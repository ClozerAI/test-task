# ClozerAI Founding Engineer Take-Home

## Real-Time AI Assistance

Your task is to build a minimal clone of ClozerAI’s **real-time assistance feature**. The goal is to demonstrate your ability to deliver a full-stack product using the required stack, while keeping the implementation lightweight and focused.

**IMPORTANT**: Keep the implementation as simple as possible.

---

## Feature Set / Scope

The application should provide the following:

1. **Authentication**

   * Users must be able to sign in using **NextAuth.js** (email/passwordless or OAuth).
   * Authenticated users can access a protected `/app` route where the functionality lives.

2. **Audio Capture from Another Tab**

   * In the browser, let the user pick an open tab and capture its **audio**.
   * Hint: Use `navigator.mediaDevices.getDisplayMedia` to capture audio.

3. **Real-Time Transcription**

   * Stream the captured audio to **Speechmatics Real-Time API**.
   * Display the live transcript in the UI, showing both partial and finalized transcriptions as they arrive.

4. **Ask & Answer**

   * Include a button labeled **“Answer the Question”**.
   * When clicked:

     * Take the latest transcript text,
     * pass it to **OpenAI API** (through Vercel's AI SDK) and:

       * Identify the **main question** asked in the transcript,
       * Generate a concise **answer**,
     * Display the answer in the app.

5. **Deployment**

   * Deploy the web app to **Vercel**.

---

## Tech Stack

Bootstrap with **T3 App** ([https://create.t3.gg/](https://create.t3.gg/)) and select:

* **Typescript**
* **Tailwind CSS:** Yes
* **tRPC:** Yes
* **Auth Provider:** NextAuth.js
* **ORM:** Drizzle
* **Next.js App Router:** Yes
* **DB:** Postgres
* **Formatting:** ESLint/Prettier

APIs/Libraries:

* **Speechmatics Real-Time** ([https://www.speechmatics.com/product/real-time](https://www.speechmatics.com/product/real-time)) for transcription
* **Vercel AI SDK** ([https://ai-sdk.dev/docs/introduction](https://ai-sdk.dev/docs/introduction)) for OpenAI API

Hosting:

* App → **Vercel**
* DB → **Vercel Postgres** or **Neon**

API Keys:

All of the services mentioned offer free trials except for the OpenAI API.

To get an OpenAI API Key, please email jure@clozerai.com.
