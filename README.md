# NOIR Café — Premium Digital Menu

A mobile-first, RTL Persian cafe/lounge menu built as a static frontend with HTML, CSS and vanilla JavaScript.

## Included

- Premium dark hospitality UI
- Persian RTL layout
- Hot drinks, cold drinks, fast food, hookah and desserts
- Signature products
- Product detail modal
- Search by product/category/ingredients/description
- Cart with quantity controls and localStorage persistence
- Checkout summary flow
- Responsive mobile/tablet/desktop layouts
- Client-side admin dashboard
- Product CRUD
- Product availability, pricing, discount, badges and Signature flags
- Category management
- Cafe settings
- Image URL replacement
- Fallback images
- Accessibility-oriented labels and focusable controls
- No backend, framework or build dependency

## Files

- `index.html` — public menu and modal/drawer shells
- `styles.css` — design system and responsive UI
- `app.js` — menu data, state, cart, search and admin logic

## Run

Open `index.html` directly in a browser, or serve the folder with any static HTTP server.

Example:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Admin

Open **مدیریت** from the footer or the settings icon on mobile.

Authentication is implemented entirely in the browser because this project intentionally has no backend. The credentials are therefore not production-grade security: anyone with access to the JavaScript source can inspect the client-side authentication logic.

All menu/settings changes are stored in the browser's localStorage. They do not synchronize between devices.

## Backend limitations

This version does not actually submit orders to a server. The checkout flow only builds a local order summary and explicitly tells the customer that no server submission occurred.

For production multi-device administration and real orders, add server-side authentication plus an API/database and replace the localStorage data layer with API calls.