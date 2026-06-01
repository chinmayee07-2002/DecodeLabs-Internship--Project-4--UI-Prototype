# FreshLeaf - Organic Food Delivery App
## High-Fidelity Interactive Prototype

A complete mobile application prototype demonstrating the full user journey for an organic food delivery service. Built with React, TypeScript, and Tailwind CSS.

---

## 🎯 Prototype Overview

This is a fully interactive prototype showcasing:
- Complete user flow from splash to order confirmation
- Real-time cart management
- Smooth page transitions
- Interactive micro-interactions
- Toast notifications
- Mobile-first responsive design

---

## 📱 User Flow

```
Splash Screen
    ↓ (Tap "Start Shopping")
Product Listing
    ↓ (Select Product)
Product Details
    ↓ (Add to Cart + Toast Notification)
Cart Screen
    ↓ (Proceed to Checkout)
Checkout
    ↓ (Place Order)
Order Confirmation
    ↓ (Continue Shopping)
Back to Product Listing
```

---

## 🖥️ Screens

### 1. Splash Screen (`/`)
**Features:**
- Hero background image
- Brand logo and name
- Tagline: "Fresh Organic Food Delivered Fast"
- Primary CTA: "Start Shopping"

**Interaction:**
- Tap "Start Shopping" → Navigate to Product Listing

**Animation:**
- Button active state (scale-98 on press)

---

### 2. Product Listing Screen (`/products`)
**Features:**
- Personalized greeting ("Good Morning")
- Search bar
- Category chips (All, Vegetables, Fruits)
- Product grid (2 columns)
- Product cards with:
  - Product image
  - Favorite icon
  - Product name & unit
  - Star rating & review count
  - Price
  - Quick add-to-cart icon
- Bottom navigation bar with cart badge

**Interactions:**
- Product card tap → Product Details
- Search bar tap → Search state (placeholder)
- Cart icon tap → Cart Screen
- Category chips → Filter state (visual feedback)
- Bottom navigation → Different sections

**Animation:**
- Product card active state (scale-98)
- Button press states
- Cart badge updates dynamically

---

### 3. Product Details Screen (`/product/:id`)
**Features:**
- Full-screen product image
- Back button
- Favorite button
- Product category badge
- Product name and price
- Star rating with review count
- Feature badges (Same Day, Certified, Premium)
- Product description
- Nutrition facts card
- Certification badges (USDA Organic, Non-GMO, Pesticide-Free)
- "You May Also Like" horizontal scroll
- Quantity selector
- Add to Cart button with price

**Interactions:**
- Back button → Navigate to Product Listing
- Quantity increment/decrement
- Add to Cart → Show success toast + Add item to cart

**Microinteractions:**
- Toast notification: "Added to Cart Successfully"
- Button press states
- Quantity selector animations

---

### 4. Cart Screen (`/cart`)
**Features:**
- Header with back button
- Item count badge
- Cart item cards with:
  - Product image
  - Product name, unit, price
  - Quantity controls
  - Delete button
- Cart summary:
  - Subtotal
  - Delivery fee (FREE)
  - Total
- "Proceed to Checkout" CTA

**Interactions:**
- Back button → Navigate to Product Listing
- Quantity controls → Update item quantity
- Delete button → Remove item from cart
- Proceed to Checkout → Navigate to Checkout

**Empty State:**
- Cart icon illustration
- "Your cart is empty" message
- "Start Shopping" button → Navigate to products

**Animation:**
- Button press states
- Item removal animation

---

### 5. Checkout Screen (`/checkout`)
**Features:**
- Header with back button
- Delivery Address section:
  - Selected address with location icon
  - Address details
  - "Change" button
- Payment Method section:
  - Credit Card option (selected)
  - Digital Wallet option
  - Radio button selections
- Order Summary section:
  - Line items with quantities
  - Subtotal, Delivery fee, Total
- "Place Order" CTA with total price

**Interactions:**
- Back button → Navigate to Cart
- Change address button → Address selector (placeholder)
- Payment method selection → Switch payment method
- Place Order → Clear cart + Navigate to Confirmation

**Animation:**
- Button press states
- Selection state changes

---

### 6. Order Confirmation Screen (`/confirmation`)
**Features:**
- Success icon with confetti emoji
- "Order Confirmed!" headline
- Confirmation message: "Your organic produce is on the way."
- Order details card:
  - Order number (randomly generated)
  - Estimated delivery time
- Notification info box
- "Continue Shopping" CTA
- "Track Order" secondary action

**Interactions:**
- Continue Shopping → Navigate to Product Listing
- Track Order → Navigate to Product Listing (placeholder)

**Animation:**
- Bouncing confetti icon
- Success icon appearance
- Button press states

---

## 🎨 Design System

### Color Palette
- **Primary Green:** `#4CAF50` (Brand, CTAs, Success)
- **Accent Yellow:** `#FFD700` (Highlights, Active states)
- **Dark Gray:** `#1F2937` (Text, Icons)
- **Medium Gray:** `#6B7280` (Secondary text)
- **Light Gray:** `#E5E7EB` (Borders, Dividers)
- **Background Beige:** `#F7F4ED` (Surface background)
- **White:** `#FFFFFF` (Cards, Containers)

### Typography
- **Headlines:** Bold, 24px-32px
- **Body:** Regular/Semibold, 14px-16px
- **Captions:** Regular, 10px-12px
- **Price:** Bold, 16px-24px in green

### Spacing
- **Card Padding:** 12px-20px
- **Section Gaps:** 12px-20px
- **Border Radius:** 12px-24px
- **Container Max Width:** 448px (mobile-first)

### Components
- **Buttons:** Rounded corners, bold text, active states
- **Cards:** White background, rounded, subtle shadows
- **Icons:** Lucide React icons, 16px-24px
- **Touch Targets:** Minimum 44px for accessibility

---

## 🔧 Technical Implementation

### Tech Stack
- **Framework:** React 18
- **Routing:** React Router 7 (Data Router pattern)
- **State Management:** React Context API
- **Styling:** Tailwind CSS v4
- **Icons:** Lucide React
- **Notifications:** Sonner (Toast library)
- **Language:** TypeScript

### Key Features
- **Cart Context:** Global cart state management
- **Dynamic Routing:** URL-based navigation with params
- **Toast Notifications:** Success feedback for cart actions
- **Responsive Design:** Mobile-first, scales to desktop
- **Accessibility:** Proper touch targets, semantic HTML

### File Structure
```
src/app/
├── App.tsx                    # Main app with router
├── routes.tsx                 # Route configuration
├── context/
│   └── CartContext.tsx        # Cart state management
├── data/
│   └── products.ts            # Product data
└── screens/
    ├── SplashScreen.tsx
    ├── ProductListingScreen.tsx
    ├── ProductDetailsScreen.tsx
    ├── CartScreen.tsx
    ├── CheckoutScreen.tsx
    └── OrderConfirmationScreen.tsx
```

---

## 🎬 Micro-Interactions

1. **Button Press States**
   - `active:scale-98` or `active:scale-95`
   - Smooth transitions (300ms ease-out)

2. **Success Toast**
   - Position: top-center
   - Duration: 2 seconds
   - Color: Success green

3. **Quantity Selector**
   - Plus/minus buttons with visual feedback
   - Number display in center

4. **Navigation Transitions**
   - Instant page transitions
   - Back button returns to previous screen

5. **Cart Badge**
   - Dynamic count update
   - Yellow background with dark text

6. **Hover/Tap Feedback**
   - All interactive elements have visual feedback
   - Opacity changes or scale transforms

---

## ♿ Accessibility Features

- ✅ Minimum 44px touch targets
- ✅ Clear visual hierarchy
- ✅ Consistent navigation patterns
- ✅ No dead-end screens (all screens have exits)
- ✅ Mobile-first interaction design
- ✅ Semantic HTML structure
- ✅ Accessible color contrast

---

## 🚀 Running the Prototype

The prototype is ready to use. Simply navigate through the app starting from the Splash Screen:

1. Click "Start Shopping" on the splash screen
2. Browse products on the listing page
3. Click any product to view details
4. Add items to cart and see the toast notification
5. View your cart via the bottom navigation
6. Proceed to checkout
7. Place your order
8. See the confirmation screen
9. Continue shopping to restart the flow

---

## 💡 Use Cases

This prototype is ideal for:
- **UI/UX Portfolio:** Demonstrate end-to-end design thinking
- **Client Presentations:** Show interactive app concepts
- **Developer Handoff:** Reference implementation for production
- **User Testing:** Validate user flows and interactions
- **Internship Projects:** Showcase comprehensive design skills

---

## 📊 Prototype Completeness

- ✅ All 6 screens implemented
- ✅ Complete user flow (Splash → Confirmation)
- ✅ Real-time cart functionality
- ✅ Interactive elements with feedback
- ✅ Toast notifications
- ✅ Mobile-responsive design
- ✅ Consistent visual design
- ✅ Accessibility considerations
- ✅ Production-ready code structure
- ✅ TypeScript type safety

---

## 🎓 Internship Presentation Tips

When presenting this prototype:

1. **Start with the user story:** "A health-conscious customer wants to order fresh organic produce..."
2. **Walk through the flow:** Demonstrate each screen in sequence
3. **Highlight interactions:** Show the cart, toast notifications, and state changes
4. **Discuss decisions:** Explain color choices, layout decisions, accessibility
5. **Show the code:** Demonstrate clean component structure and state management
6. **Mention scalability:** Discuss how this could expand (more products, user accounts, order tracking)

---

**Created for UI/UX Internship Portfolio**
**Stack:** React + TypeScript + Tailwind CSS + React Router
**Type:** High-Fidelity Interactive Prototype
