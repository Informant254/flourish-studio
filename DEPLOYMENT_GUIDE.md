# Deployment Guide

## Quick Start (5 minutes)

### 1. Netlify Deployment (Recommended)

```bash
# Step 1: Go to https://netlify.com
# Step 2: Sign up with Gmail
# Step 3: Click "Add new site" → "Deploy manually"
# Step 4: Drag index.html onto the upload area
# Step 5: Wait ~10 seconds
# Your store is LIVE! ✅
```

**Your URL:** `https://your-project-name.netlify.app`

### 2. GitHub Pages Deployment

```bash
# If you have Git installed:
git clone <your-repo-url>
cd flourish-studio

# Push to GitHub Pages
# (GitHub automatically serves index.html)
```

**Your URL:** `https://yourusername.github.io/flourish-studio`

### 3. Vercel Deployment (Alternative)

```bash
# Go to https://vercel.com
# Import from GitHub
# Deploy in 1 click
```

## Customization Steps

### Before Deploying

1. **Update Payment Links**
   - Find the `CHECKOUT_URL` constant in `index.html`
   - Replace it with your Selar, Gumroad, or Payhip product link
   - Test the checkout flow on mobile and desktop

2. **Add Your Products**
   - Update product names
   - Update product descriptions
   - Update product prices
   - Add/remove products as needed

3. **Update Testimonials**
   - Replace the placeholder trust cards with real customer quotes once you have them
   - Keep at least 1-2 cards visible

4. **Customize Colors** (Optional)
   - Find `:root { }` in the CSS
   - Change hex color codes to match your brand

5. **Update Footer**
   - Add your real email/contact info
   - Update social media links if desired

### Testing

Before deploying, test locally:
1. Open `index.html` in your browser
2. Click all "Buy Now" buttons
3. Verify they redirect correctly
4. Test on mobile device
5. Check all links work

## Production Checklist

- [ ] Update Selar links to YOUR products
- [ ] Test all Buy Now buttons
- [ ] Verify payment flow works
- [ ] Replace testimonials with real reviews (once available)
- [ ] Update footer with correct info
- [ ] Test on mobile
- [ ] Deploy to Netlify/Vercel
- [ ] Share URL on social media
- [ ] Monitor for first sales

## Adding Products

To add a new product:

```html
<div class="product-card">
  <div class="product-emoji">🎯</div>
  <div class="product-tag">Category</div>
  <h3>Product Name</h3>
  <p>Product description goes here.</p>
  <div class="product-footer">
    <div class="product-price">$XX</div>
    <a href="YOUR_SELAR_LINK" target="_blank">
      <button class="buy-btn">Buy Now</button>
    </a>
  </div>
</div>
```

## Troubleshooting

**Issue: Buy buttons don't redirect**
- Check the Selar link is correct
- Make sure `target="_blank"` is in the link
- Test on different browser

**Issue: Store looks broken on mobile**
- Clear browser cache (Ctrl+Shift+Delete)
- Test in Incognito mode
- Try different browser

**Issue: Images not loading**
- Make sure `journal_thumbnail.png` is in same folder as `index.html`
- Check image file name spelling

**Issue: Styles look wrong**
- Clear browser cache
- Check CSS hasn't been modified

## Performance Tips

1. **Compress images** before uploading
2. **Minify CSS** if you modify it
3. **Cache busting** — rename files if updating
4. **CDN** — Netlify handles this automatically

## Security

- No sensitive data stored in HTML
- No passwords in code
- Use HTTPS (Netlify provides automatically)
- No database = no hacking risk

## Next Steps After Launch

1. **Monitor traffic** — Netlify provides analytics
2. **Collect reviews** — Ask early buyers for feedback
3. **Track sales** — Check your M-Pesa/Selar dashboard
4. **Iterate** — Update based on customer feedback
5. **Scale** — Add more products once first one succeeds

## Support

If deployment issues occur:
1. Check Netlify/Vercel error messages
2. Verify all links are correct
3. Clear cache and reload
4. Try different browser
5. Check file permissions

---

**You're ready to go live! 🚀**

Remember: The moment you deploy, you're in business. Your first customer could find you today.

Good luck!
