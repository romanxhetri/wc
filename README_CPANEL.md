# Deployment to WordPress cPanel

To deploy this application to your cPanel hosting:

1.  **Build the application**: Run `npm run build` in your local environment.
2.  **Locate the `dist` folder**: This folder contains all the static files needed for your website.
3.  **Upload to cPanel**:
    *   Log in to your cPanel.
    *   Open **File Manager**.
    *   Navigate to your website's root directory (usually `public_html`).
    *   If you want to host it in a subdirectory (e.g., `example.com/app`), create a folder named `app` and upload the contents of the `dist` folder there.
    *   If you want it at the root, upload the contents of `dist` directly into `public_html`.
4.  **Routing**: The `.htaccess` file included in the `public` folder will handle routing for you. It ensures that when you refresh a page, it doesn't return a 404 error.

### Note on WordPress
If you are hosting this alongside a WordPress installation:
*   Ensure that the `.htaccess` rules don't conflict with WordPress's rules.
*   The provided `.htaccess` is designed for a standalone React app. If you're putting this in a subdirectory of a WordPress site, it should work fine within that folder.
