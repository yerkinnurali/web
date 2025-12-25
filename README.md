# Creative Portfolio & Booking System

A fully functional web application for showcasing creative portfolios and managing client bookings, built with HTML5, CSS3, JavaScript, PHP, and MySQL.

## Features

- **Dark Theme Design**: Modern dark theme with smooth transitions
- **Responsive Layout**: Mobile-friendly design using Flexbox
- **Dynamic Portfolio Gallery**: Filterable and sortable portfolio items
- **Interactive Booking System**: AJAX-powered booking form
- **Web Services**: RESTful API endpoints for data exchange
- **Session Management**: User state and theme preferences

## Project Structure

```
/
├── index.php              # Home page
├── about.php              # About page
├── portfolio.php          # Portfolio & booking page
├── process_booking.php    # Server-side form processing
├── .htaccess             # Apache configuration
├── assets/
│   ├── css/
│   │   ├── style.css     # Base styles
│   │   ├── dark.css       # Dark theme
│   │   └── light.css      # Light theme
│   └── js/
│       ├── data.js        # Data management & API calls
│       ├── ui.js          # DOM manipulation
│       └── events.js      # Event handlers
├── includes/
│   ├── config.php        # Database configuration
│   ├── header.php         # Header template
│   └── footer.php         # Footer template
├── api/
│   ├── portfolio.php     # Web Service v1 (GET)
│   ├── booking.php       # Web Service v2 (POST)
│   └── theme.php         # Theme preference API
└── data/
    └── schema.sql        # Database schema
```

## Installation

1. **Database Setup**:
   - Import `data/schema.sql` into MySQL
   - Update database credentials in `includes/config.php`

2. **Server Configuration**:
   - Place files in XAMPP `htdocs` directory
   - Ensure Apache and MySQL are running
   - PHP 7.4+ required

3. **Access the Application**:
   - Open browser: `http://localhost/`
   - Navigate to portfolio page to view items and submit bookings
## Usage

1. **View Portfolio**: Navigate to Portfolio page to see all items
2. **Filter Items**: Click category buttons to filter by type
3. **Sort Items**: Use dropdown to sort by date, title, or category
4. **Submit Booking**: Fill out the booking form (submitted via AJAX)
5. **Toggle Theme**: Click theme toggle button to switch between dark/light

## API Endpoints

### GET /api/portfolio.php
Returns all portfolio items in JSON format.

### POST /api/booking.php
Accepts booking data and inserts into database.

**Request Body:**
```json
{
  "client_name": "John Doe",
  "client_email": "john@example.com",
  "client_phone": "123-456-7890",
  "service_type": "Wedding Cake",
  "event_date": "2024-12-25",
  "event_time": "14:00",
  "message": "Additional details"
}
```

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Edge (latest)
- Safari (latest)

## Notes

- Ensure MySQL is running before accessing the application
- Database credentials should be updated in `includes/config.php`
- All forms use AJAX submission (no page reloads)
- Theme preference is saved in cookies

