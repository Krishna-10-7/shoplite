# ShopLite

A small shop (product page, cart, checkout and a JSON API) used as the app under test for [SentinelQA](https://github.com/Krishna-10-7/build).

```bash
npm install
npm start            # http://localhost:4100, PORT and HOST are honoured
```

## Release branches

Each branch is a realistic change on top of `main`. Some only change markup, some ship a bug. The test suite (ticket SHOP-42) should heal the first kind and fail on the second.

| Branch | What changed | Kind |
|---|---|---|
| `redesign/add-to-bag` | New design system: test ids renamed, "Add to cart" becomes "Add to bag" | markup only |
| `redesign/compare-button` | New "Add to compare" button next to Add to cart; its test id was renamed | markup only |
| `bug/cart-total` | Cart total is computed from catalogue prices and ignores quantity | bug |
| `bug/wishlist-swap` | Redesign that also swaps the Add to cart and Add to wishlist labels | bug |
| `bug/order-500` | New shipping-note feature crashes the order API | bug |
