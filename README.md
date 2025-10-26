# Paul Zografakis Art Portfolio Website

A minimalist, elegant portfolio website inspired by Hauser & Wirth gallery aesthetic.

## Structure

- `index.html` - Main gallery page with 20 artwork slots
- `about.html` - Biography, CV, exhibitions
- `archive.html` - Performance, installation, and video archive
- `contact.html` - Contact information and form
- `artwork.html` - Individual artwork detail page template
- `styles.css` - All styling
- `script.js` - JavaScript for interactivity
- `images/` - Folder for all artwork images

## How to Add Your Images

### Image Requirements
- **Format:** JPG or PNG recommended
- **Gallery thumbnails:** Ideally 800-1200px width
- **Detail images:** 1500-2500px width for high quality
- **Aspect ratio:** 3:4 portrait works best for the grid layout

### Naming Convention
Save your images in the `images/` folder with these names:
- `placeholder-1.jpg` through `placeholder-20.jpg` for gallery thumbnails
- `artist-photo.jpg` for your portrait on the About page
- Add larger detail versions if needed

### Steps to Add Images

1. **Prepare your images:**
   - Resize/optimize for web (use tools like Photoshop, GIMP, or online compressors)
   - Save with descriptive names

2. **Upload to the images folder:**
   - Place all images in the `/images` directory

3. **Update the HTML:**
   - In `index.html`, find each artwork item
   - Update the `src` attribute to match your image filename
   - Update the `alt` text with artwork title
   - Update the artwork title and medium text

Example:
```html
<div class="artwork-item">
    <a href="artwork.html?id=1">
        <div class="artwork-image-container">
            <img src="images/my-painting-2024.jpg" alt="Blue Composition" class="artwork-image">
        </div>
        <div class="artwork-info">
            <h3>Blue Composition</h3>
            <p>Oil on canvas, 2024</p>
        </div>
    </a>
</div>
```

## How to Customize Content

### About Page (`about.html`)
1. Add your artist photo as `images/artist-photo.jpg`
2. Replace placeholder text with your bio
3. Update exhibitions, education, awards sections with your information

### Archive Page (`archive.html`)
1. Add your performance, installation, and video work titles
2. Include year, venue, and other relevant details
3. Optionally add links to documentation

### Contact Page (`contact.html`)
1. Update email, Instagram, studio location
2. To make the form functional, integrate with:
   - Formspree (https://formspree.io/)
   - Netlify Forms (if hosting on Netlify)
   - Your own backend

### Individual Artwork Pages (`artwork.html`)
1. Edit the `artworks` object in the script section
2. Add details for each piece: title, medium, year, dimensions, description
3. Make sure the `id` parameter matches the gallery links

Example:
```javascript
const artworks = {
    '1': {
        title: 'Blue Composition',
        medium: 'Oil on canvas',
        year: '2024',
        dimensions: '48 × 36 inches',
        description: 'This painting explores...',
        image: 'images/blue-composition.jpg'
    },
    // Add more artworks...
};
```

## Deploying to Vercel

1. Push all files to your GitHub repository
2. Vercel will automatically detect changes and redeploy
3. Your site will be live at: artzog-com.vercel.app

## Connecting Your Custom Domain

Once you're ready to use your Namecheap domain:

1. In Vercel dashboard, go to your project
2. Click "Settings" → "Domains"
3. Add your domain (artzog.com)
4. Follow Vercel's instructions to update DNS in Namecheap
5. Wait for DNS propagation (can take up to 48 hours)

## Color Customization

To change colors, edit `styles.css`:
- Background: `background-color: #fff;` (currently white)
- Text: `color: #000;` (currently black)
- Borders: `border-color: #e0e0e0;` (currently light gray)
- Links hover: `.opacity` in the hover states

## Support

For questions about:
- **Vercel deployment:** https://vercel.com/docs
- **HTML/CSS editing:** https://developer.mozilla.org/
- **GitHub:** https://docs.github.com/

## Next Steps

1. Add your artwork images
2. Customize all text content
3. Test on different devices
4. Connect your custom domain
5. Share your portfolio!
