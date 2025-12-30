# Salero Awak - Nasi Padang Restaurant Website

A modern, interactive website for a Nasi Padang restaurant featuring online menu browsing, shopping cart functionality, and integrated checkout system.

## Project Overview

This website was developed as a final project (UAS) for Multimedia Technology course. It showcases a complete restaurant web application with modern features including dynamic product management, shopping cart, and customer interaction capabilities.

**Note:** The background banner image is not included in this repository due to its large file size.

## Technologies Used

- **HTML5** - Structure and semantic markup
- **CSS3** - Styling and responsive design
- **JavaScript (ES6+)** - Interactive functionality
- **Alpine.js** - Reactive data binding and state management
- **Font Awesome** - Icon library
- **Google Fonts** - Poppins font family

## Features

### 1. Navigation System
- **Responsive Navigation Bar**: Features a sticky navigation bar with links to all major sections (Home, About, Menu, Products, Contact)
- **Hamburger Menu**: Mobile-friendly collapsible menu for smaller screens that toggles visibility when clicked
- **Active State Management**: Automatically closes navigation when clicking outside the menu area
- **Brand Logo**: Displays "Salero Awak" branding prominently in the navbar

### 2. Search Functionality
- **Search Form**: Toggle-able search form that appears when clicking the search icon
- **Focus Management**: Automatically focuses on the search input field when opened
- **Click-Outside Detection**: Closes the search form when clicking outside its area
- **Search Box**: Input field with placeholder text for user queries

### 3. Shopping Cart System
- **Dynamic Cart**: Real-time shopping cart powered by Alpine.js state management
- **Add to Cart**: Adds products to cart with automatic quantity tracking
- **Quantity Adjustment**: Increment (+) and decrement (-) buttons to modify item quantities
- **Cart Badge**: Displays total item count on the cart icon
- **Price Calculation**: Automatically calculates individual item totals and cart grand total
- **Currency Formatting**: Displays prices in Indonesian Rupiah (IDR) format
- **Empty Cart Detection**: Shows "Cart Is Empty" message when no items are present
- **Persistent State**: Maintains cart state during browsing session

### 4. Hero Section
- **Welcome Banner**: Eye-catching hero section with restaurant tagline "Pedas Gurih Penuh Cerita" (Spicy, Savory, Full of Stories)
- **Audio Player**: Interactive audio player with play/pause functionality
  - Toggle button that changes text between "Play Audio" and "Pause Audio"
  - Plays traditional Minang music (minag.mp3)
  - Automatically resets when audio ends
  - Powered by Alpine.js for state management
- **Restaurant Description**: Brief introduction to the restaurant's authentic Minang cuisine

### 5. About Section
- **YouTube Video Embed**: Responsive embedded video showcasing the restaurant
- **Responsive Design**: Video iframe scales to 100% width and height on different devices
- **Content Description**: Explains why customers should choose the restaurant
- **Quality Messaging**: Highlights use of fresh, high-quality ingredients
- **Video Attribution**: Copyright notice for midnight_studio 2021

### 6. Menu Display
- **Menu Cards**: Grid layout displaying 6 signature dishes
- **Product Images**: Visual representation of each dish
- **Dish Names**: Clear labeling of menu items (Rendang, Ayam Bakar, Ikan Bakar, Telur Barendo, Gulai Tunjang, Gulai Kepala Ikan)
- **Pricing**: Displays prices in IDR for each menu item
- **Responsive Grid**: Adapts to different screen sizes

### 7. Products Section
- **Dynamic Product Rendering**: Uses Alpine.js to dynamically generate product cards from a data array
- **Product Data Management**: Centralized product data including id, name, image, and price
- **Quick Add to Cart**: One-click add to cart functionality on each product card
- **Product Images**: Visual display of products from the products directory
- **Price Display**: Formatted currency display for each product
- **6 Products Available**: Rendang (30K), Ayam Bakar (20K), Ikan Bakar (25K), Telur Barendo (10K), Gulai Tunjang (40K), Gulai Kepala Ikan (25K)

### 8. Checkout System
- **Customer Information Form**: Collects name, email, and phone number
- **Form Validation**: Real-time validation that enables checkout button only when all fields are filled
- **WhatsApp Integration**: Sends order details directly to WhatsApp (6285218589706)
- **Order Formatting**: Automatically formats order message with customer details and item breakdown
- **Hidden Fields**: Stores cart items and total in hidden form fields
- **Disabled State**: Checkout button remains disabled until form is properly completed
- **Loading States**: Visual feedback during form submission

### 9. Contact Form
- **Google Form Integration**: Submits contact information to Google Sheets via Google Apps Script
- **Input Fields**: Collects customer name, email, and phone number
- **Form Icons**: Font Awesome icons for visual enhancement (user, envelope, phone)
- **Loading Indicator**: Shows "Mengirim..." (Sending...) state during submission
- **Success/Error Handling**: Alert messages for successful submission or errors
- **Form Reset**: Automatically clears form after successful submission
- **Disabled Button State**: Prevents multiple submissions

### 10. Google Maps Integration
- **Location Display**: Embedded Google Maps showing restaurant location
- **Interactive Map**: Users can zoom, pan, and interact with the map
- **Politeknik Negeri Jakarta Location**: Shows the institution's location as reference
- **Lazy Loading**: Maps load efficiently with lazy loading attribute
- **Responsive Embed**: Map adapts to different screen sizes

### 11. Social Media Integration
- **Social Links**: Footer includes links to Instagram, Twitter (X), TikTok, and WhatsApp
- **Font Awesome Icons**: Professional social media icons
- **Multiple Channels**: Provides various ways for customers to connect

### 12. Footer
- **Navigation Links**: Quick access to all main sections
- **Social Media Icons**: Links to Instagram, Twitter, TikTok, and WhatsApp
- **Credits**: Attribution to Kelompok2 (Group 2) with copyright 2024
- **Responsive Design**: Adapts to different screen sizes

### 13. Modal System
- **Item Detail Modal**: Placeholder for detailed product information
- **Close Functionality**: Can be closed by clicking the close icon or outside the modal
- **Flexible Display**: Shows/hides based on user interaction
- **Event Prevention**: Prevents default link behavior

### 14. Interactive JavaScript Features
- **Click Outside Detection**: Closes active menus when clicking elsewhere on the page
- **Toggle Functions**: Opens and closes various UI elements (search, cart, navigation)
- **Event Listeners**: Handles multiple user interactions across the site
- **State Management**: Maintains UI state for better user experience

## Project Structure

```
UAS/
├── index.html          # Main HTML file
├── css/
│   └── style.css      # Main stylesheet
├── js/
│   └── script.js      # UI interaction scripts
├── src/
│   └── app.js         # Alpine.js store and product data
├── img/
│   ├── menu/          # Menu item images
│   ├── products/      # Product images
│   └── tentang-kami.jpg
├── audio/
│   └── minag.mp3      # Traditional Minang music
├── fontawesome/       # Font Awesome icon library
└── README.md          # This file
```

## Installation & Setup

1. Clone this repository:
```bash
git clone https://github.com/EkaMiharja/UAS.git
```

2. Navigate to the project directory:
```bash
cd UAS
```

3. Open `index.html` in a web browser:
```bash
# On macOS
open index.html

# On Linux
xdg-open index.html

# On Windows
start index.html
```

No build process or dependencies installation required - this is a static website that runs directly in the browser.

## Configuration

### WhatsApp Integration
To change the WhatsApp number for checkout, edit line 100 in `src/app.js`:
```javascript
window.open('http://wa.me/YOUR_NUMBER?text=' + encodeURIComponent(message));
```

### Google Form Integration
To update the Google Form submission endpoint, modify line 208 in `index.html`:
```javascript
const scriptURL = 'YOUR_GOOGLE_APPS_SCRIPT_URL';
```

### Product Data
To add or modify products, edit the items array in `src/app.js`:
```javascript
items: [
    {id: 1, name: 'Product Name', img: 'image.jpg', price: 30000 },
    // Add more items here
]
```

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Credits

- **Development Team**: Kelompok2 (Group 2)
- **Institution**: Politeknik Negeri Jakarta
- **Year**: 2024
- **Video Content**: midnight_studio 2021
- **Font**: Poppins by Google Fonts
- **Icons**: Font Awesome

## License

This project was created for educational purposes as part of the Multimedia Technology course final examination (UAS).

## Contact

For inquiries or support, please use the contact form on the website or reach out through the social media channels provided in the footer.
