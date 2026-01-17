# Deployment Instructions

This folder (`frontend-deploy`) contains a standalone copy of the requested frontend application, ready for deployment.

## Pushing to a New GitHub Repository

1.  **Create a new repository** on GitHub (e.g., `astraguard-frontend`).
2.  **Push the code**:
    ```bash
    cd frontend-deploy
    git remote add origin https://github.com/YOUR_USERNAME/NEW_REPO_NAME.git
    git branch -M main
    git push -u origin main
    ```

## Deploying to Vercel

1.  Go to [Vercel Dashboard](https://vercel.com/dashboard).
2.  Click **"Add New..."** -> **"Project"**.
3.  Import the GitHub repository you just created (`astraguard-frontend`).
4.  **Configure Project**:
    *   **Framework Preset**: Next.js (should detect automatically).
    *   **Root Directory**: `./` (default).
    *   **Build Command**: `next build` (default).
    *   **Install Command**: `npm install` (default).
5.  Click **Deploy**.

## Local Testing (Optional)

You can test this build locally before pushing:

```bash
cd frontend-deploy
npm install
npm run build
npm start
```
