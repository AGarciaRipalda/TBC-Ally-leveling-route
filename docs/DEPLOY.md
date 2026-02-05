# Deployment to Render

This project is configured to be easily deployed to [Render.com](https://render.com) using a Blueprint.

## Prerequisites

1.  A GitHub account.
2.  A [Render](https://render.com) account (you can sign up with GitHub).
3.  This repository pushed to your GitHub.

## Steps to Deploy

1.  **Push to GitHub**: Ensure all your local changes (including `render.yaml`) are pushed to your GitHub repository.
    ```bash
    git add .
    git commit -m "Prepare for Render deployment"
    git push origin master
    ```

2.  **Create New Blueprint Instance**:
    *   Go to your [Render Dashboard](https://dashboard.render.com/).
    *   Click on the **New +** button in the top right corner.
    *   Select **Blueprint**.
    *   Connect your GitHub account if you haven't already.
    *   Select the `TBC-Ally-leveling-route` repository from the list.

3.  **Approve and Deploy**:
    *   Render will read the `render.yaml` file from your repository.
    *   It will show you the service it's about to create (`tbc-leveling-logbook`).
    *   Click **Apply**.

Render will now deploy your site. Once finished, you will get a URL (like `https://tbc-leveling-logbook.onrender.com`) where your logbook is live!

## Manual Deployment (Alternative)

If you prefer not to use the Blueprint:

1.  Go to Render Dashboard -> New -> **Static Site**.
2.  Select your repository.
3.  **Name**: `tbc-leveling-logbook` (or whatever you want).
4.  **Branch**: `master`.
5.  **Root Directory**: `.` (leave empty).
6.  **Build Command**: (leave empty).
7.  **Publish Directory**: `.` (dot) or leave empty if it defaults to root.
8.  Click **Create Static Site**.
