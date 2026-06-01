# 🚀 Quick Start Guide

## Using the Prototype

The FreshLeaf prototype is ready to use! Here's how to navigate:

### Starting Point
The app automatically starts at the **Splash Screen** (`/`)

### Navigation Flow

1. **Splash Screen** → Click "Start Shopping"
2. **Product Listing** → Click any product card
3. **Product Details** → Click "Add to Cart"
   - Watch for the success toast notification!
   - Adjust quantity with +/- buttons
4. **Cart** (via bottom nav cart icon)
   - Adjust quantities
   - Remove items
   - Click "Proceed to Checkout"
5. **Checkout** → Click "Place Order"
6. **Order Confirmation** → Click "Continue Shopping"

### Key Features to Try

✅ **Add Multiple Products**
- Go back to product listing and add more items
- Watch the cart badge update

✅ **Manage Cart**
- Increase/decrease quantities
- Remove items
- See real-time price updates

✅ **Complete Flow**
- Go through entire journey from splash to confirmation
- Notice smooth transitions between screens

✅ **Interactive Elements**
- All buttons have press states
- Toast notifications for feedback
- Dynamic cart badge
- Quantity selectors

### Screen URLs (for direct access)

```
/                  → Splash Screen
/products          → Product Listing
/product/1         → Strawberries Details
/product/2         → Avocados Details
/product/3         → Carrots Details
/product/4         → Broccoli Details
/cart              → Shopping Cart
/checkout          → Checkout
/confirmation      → Order Confirmation
```

### Pro Tips

💡 **For Presentations:**
- Start fresh by clearing cart (remove all items)
- Walk through the flow step-by-step
- Highlight the toast notification when adding to cart
- Show the dynamic cart badge updating

💡 **For Testing:**
- Try adding same product multiple times
- Test empty cart state
- Navigate back and forth between screens
- Adjust quantities in cart

💡 **For Development:**
- All screens are in `src/app/screens/`
- Cart state in `src/app/context/CartContext.tsx`
- Routes in `src/app/routes.tsx`
- Product data in `src/app/data/products.ts`

---

## Mobile View

The prototype is optimized for mobile (9:19.5 aspect ratio).

**Best viewed in:**
- Mobile device
- Browser DevTools mobile view
- 375px wide viewport
- Portrait orientation

---

## Interactions Checklist

✅ Splash → Products navigation  
✅ Product card click → Details  
✅ Add to cart with toast  
✅ Cart badge updates  
✅ Quantity increment/decrement  
✅ Cart management  
✅ Checkout flow  
✅ Order confirmation  
✅ Continue shopping loop  

---

## Need Help?

See `PROTOTYPE_README.md` for full documentation  
See `PRESENTATION_BRIEF.md` for presentation guide
