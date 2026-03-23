# GlowSteps Shopify Store — Admin Setup Guide

Complete this checklist in your Shopify Admin after uploading the theme.

---

## STEP 1 — Upload & Activate Theme

1. Go to **Online Store → Themes**
2. Click **Add theme → Upload ZIP file** and upload the theme ZIP
3. Click **Publish** to activate

---

## STEP 2 — Create Navigation Menus

Go to **Online Store → Navigation**

### Main Menu (for header)
Create a menu named `main-menu` with these links:
| Title | Link |
|---|---|
| Bags | /collections/bags |
| Shoes | /collections/shoes |
| Sale | /collections/sale |
| New Arrivals | /collections/new-arrivals |

### Footer Menu
Create a menu named `footer` with these links:
| Title | Link |
|---|---|
| Bags | /collections/bags |
| Shoes | /collections/shoes |
| Sale | /collections/sale |
| New Arrivals | /collections/new-arrivals |
| About Us | /pages/about-us |
| Contact | /pages/contact |

---

## STEP 3 — Create Collections

Go to **Products → Collections** and create these 4 collections:

| Collection Name | Handle (URL) | Condition |
|---|---|---|
| Bags | bags | Tag equals "bags" |
| Shoes | shoes | Tag equals "shoes" |
| Sale | sale | Compare at price is greater than price |
| New Arrivals | new-arrivals | Tag equals "new" |

> Use **Automated collections** with the conditions above, or manually add products.

---

## STEP 4 — Add Products

Go to **Products → Add product** and add these 8 products:

| Product Name | Price | Tags | Collection |
|---|---|---|---|
| Structured Tote Bag | Rs. 1,800 | bags, new | Bags |
| Crossbody Mini Bag | Rs. 1,200 | bags, sale | Bags, Sale |
| Leather Shoulder Bag | Rs. 2,800 | bags, hot | Bags |
| Clutch Evening Bag | Rs. 1,500 | bags, new | Bags |
| Block Heel Sandals | Rs. 2,200 | shoes | Shoes |
| Embroidered Khusse | Rs. 1,500 | shoes, hot | Shoes |
| Stiletto Heels | Rs. 2,500 | shoes, sale | Shoes, Sale |
| Casual Flat Sandals | Rs. 900 | shoes, new | Shoes |

**For Sale products** — set a **Compare at price** higher than the Price.

---

## STEP 5 — Currency Settings

Go to **Settings → Store details**
- **Currency:** PKR — Pakistani Rupee
- **Country/Region:** Pakistan

---

## STEP 6 — Payment Methods

Go to **Settings → Payments**

1. **Cash on Delivery (COD)**
   - Scroll to **Manual payment methods**
   - Click **Add manual payment method**
   - Select **Cash on Delivery (COD)**

2. **JazzCash**
   - In Manual payment methods, click **Create custom payment method**
   - Name: `JazzCash`
   - Add instructions: "Send payment to JazzCash account [YOUR NUMBER] and share screenshot on WhatsApp."

3. **EasyPaisa**
   - In Manual payment methods, click **Create custom payment method**
   - Name: `EasyPaisa`
   - Add instructions: "Send payment to EasyPaisa account [YOUR NUMBER] and share screenshot on WhatsApp."

---

## STEP 7 — Shipping Zones

Go to **Settings → Shipping and delivery**

1. Click **Manage rates** under Shipping
2. Under **Domestic** (or create a zone called **Pakistan**):
   - **Add rate:** Flat rate — Name: `Standard Delivery` — Price: Rs. 250
   - **Add rate:** Free shipping — Name: `Free Delivery (Rs. 3000+)` — set condition: Order price ≥ Rs. 3,000

---

## STEP 8 — Update WhatsApp Number in Footer

Go to **Online Store → Themes → Customize**
1. Click on the **Footer** section
2. Find the **Contact Us** text block
3. Replace `+92-XXX-XXXXXXX` with your actual WhatsApp number

---

## STEP 9 — Upload Logo

Go to **Online Store → Themes → Customize → Header**
1. Upload your GlowSteps logo (PNG, transparent background recommended)
2. Set width to **110px**

---

## STEP 10 — Add Pages

Go to **Online Store → Pages** and create:
- **About Us** — paste about text
- **Contact** — use the contact template

---

## STEP 11 — Checkout Settings

Go to **Settings → Checkout**
- Enable **Phone number** field (required for COD)
- Add to the **Order status page** field:
  ```
  <p>Thank you for shopping with GlowSteps! For COD orders, our team will call you to confirm.</p>
  <p>WhatsApp: +92-XXX-XXXXXXX</p>
  ```

---

## STEP 12 — Instagram Feed (Optional)

To show a real Instagram feed, install a free app:
- **Instafeed** (free) — search in Shopify App Store
- After installing, the app will replace the placeholder section on the homepage

---

## Files Modified by This Setup

| File | What Changed |
|---|---|
| `config/settings_data.json` | Brand colors (gold/cream), heading scale 1.2x, Cormorant + Jost fonts |
| `templates/index.json` | 8 homepage sections in correct order |
| `sections/header-group.json` | Dark header (#1A1A1A), gold announcement bar, delivery text |
| `sections/footer-group.json` | Footer links, contact block, dark theme |
| `templates/collection.json` | Vertical filter sidebar, quick-add buttons, 4-column grid |
| `layout/theme.liquid` | Loads glowsteps-custom.css |
| `assets/glowsteps-custom.css` | All brand CSS: gold prices, hover colors, sticky mobile cart |

---

*GlowSteps — Premium Ladies Bags & Shoes, Pakistan*
