# MARKET EXPRESS — Separate Admin Website

Suggested GitHub repository: `market-express-admin`

## Deploy
1. Create a separate GitHub repository named `market-express-admin`.
2. Upload every file in this ZIP to the repository root.
3. In Settings → Pages, deploy from `main` and `/ (root)`.
4. Enable Email/Password Authentication in Firebase.
5. Authorize the admin site's GitHub Pages domain in Firebase Authentication.
6. Give the owner's account the Firebase custom claim `admin: true` using the trusted Admin SDK script. Follow the included script instructions; never put service-account credentials in this repository or in browser JavaScript.
7. Review the included Firestore and Storage rules against the existing marketplace's rules before deploying. Do not blindly replace rules needed by checkout, reviews, or existing product uploads.

This website uses the shared Firebase project `enitan-collection-7e541`. The admin dashboard reviews `sellerApplications` and pending documents in `products`, and updates seller/product approval status.

Admin URL after deployment:
`https://YOUR-GITHUB-USERNAME.github.io/market-express-admin/admin-sellers.html`

The root `index.html` redirects to the admin page. The dashboard is not secured merely because its URL is separate or hard to guess; the Firebase admin custom claim and restrictive rules are essential.

## Other MARKET EXPRESS websites
- Main storefront: https://oluwabukunmiabraham7-rgb.github.io/Market-expres/
- Seller applications: https://oluwabukunmiabraham7-rgb.github.io/market-express-seller-apply/seller-apply.html
- Seller upload dashboard: https://oluwabukunmiabraham7-rgb.github.io/market-express-seller-dashboard/seller.html
- Admin website: https://oluwabukunmiabraham7-rgb.github.io/market-express-admin/admin-sellers.html

These are suggested URLs. They become active only after you create the repositories with the exact names above and GitHub Pages finishes deploying. If your GitHub username differs, replace it in the links.
