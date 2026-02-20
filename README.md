# Cookies and Local Storage Project

This project demonstrates the use of cookies, local storage, and session storage in web development. It includes multiple tasks that progressively build understanding of browser storage mechanisms.

## 📋 Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Tasks Overview](#tasks-overview)
- [Task Details](#task-details)

## 🚀 Installation

1. Clone the repository or navigate to the project directory:
```bash
cd Cookies_local_storage
```

2. Install dependencies:
```bash
npm install
```

## 💻 Usage

Start the development server:
```bash
node_modules/.bin/webpack-dev-server
```

Or use the npm script:
```bash
npm run dev
```

The server will start on `http://localhost:8080`

## 📚 Tasks Overview

| Task | File | Description |
|------|------|-------------|
| 0 | `0-index.html` | Basic cookie creation and display |
| 1 | `1-index.html` | Cookies with 10-day expiration |
| 2 | `2-index.html` | Cookie retrieval function |
| 3 | `3-index.html` | Login form with cookie-based authentication |
| 4 | `4-index.html` | Using js-cookie library |
| 5 | `5-index.html` | Shopping cart with Local Storage |
| 6 | `6-index.html` | Shopping cart with Session Storage |
| 7 | `7-index.html` | Advanced cart system with quantities |

## 📖 Task Details

### Task 0: Create Basic Cookie
**File:** `0-index.html`

- Creates a basic HTML form with firstname and email inputs
- Two buttons: "Log me in" and "Show the cookies"
- `setCookies()`: Sets cookies for firstname and email
- `showCookies()`: Displays all cookies in a paragraph

**Access:** http://localhost:8080/0-index.html

### Task 1: Cookies with 10-Day Expiration
**File:** `1-index.html`

- Reuses code from Task 0
- Modifies cookie expiration to 10 days instead of 1 day

**Access:** http://localhost:8080/1-index.html

### Task 2: Cookie Retrieval Function
**File:** `2-index.html`

- Reuses code from Task 1
- `getCookie(name)`: Retrieves a specific cookie value by name
- Modified `showCookies()`: Displays formatted cookie values

**Access:** http://localhost:8080/2-index.html

### Task 3: Login Form with Authentication
**File:** `3-index.html`

- Login form with firstname and email inputs
- `showForm()`: Displays the login form
- `hideForm()`: Hides the login form
- `deleteCookiesAndShowForm()`: Removes cookies and shows form
- `showWelcomeMessageOrForm()`: Checks authentication status
  - If logged in: Shows "Welcome FIRSTNAME (logout)" message
  - If not logged in: Shows login form
- Welcome message built entirely with JavaScript

**Access:** http://localhost:8080/3-index.html

### Task 4: Using js-cookie Library
**File:** `4-index.html`

- Uses js-cookie library via CDN (jsdelivr)
- Replaces custom `getCookie()` with `Cookies.get()`
- Uses `Cookies.set()` in `setCookiesAndShowWelcomeMessage()`
- Uses `Cookies.remove()` in `deleteCookiesAndShowForm()`

**Access:** http://localhost:8080/4-index.html

### Task 5: Shopping Cart with Local Storage
**File:** `5-index.html`

- Array of available items: Shampoo, Soap, Sponge, Water
- Checks for Local Storage support
- `addItemToCart(item)`: Adds item to Local Storage
- `createStore()`: Creates clickable list of products
- `displayCart()`: Shows message with previous cart items count
- **Key Feature:** Data persists across browser sessions and tabs

**Access:** http://localhost:8080/5-index.html

### Task 6: Shopping Cart with Session Storage
**File:** `6-index.html`

- Same structure as Task 5
- Uses Session Storage instead of Local Storage
- **Key Feature:** Data only persists for the current tab/session
- Opening a new tab shows empty cart

**Access:** http://localhost:8080/6-index.html

### Task 7: Advanced Cart System
**File:** `7-index.html`

- Advanced shopping cart with quantity management
- Uses Session Storage with JSON serialization
- `getCartFromStorage()`: Parses cart from Session Storage
- `addItemToCart(item)`: Adds item with quantity tracking
- `removeItemfromCart(item)`: Removes specific item
- `clearCart()`: Clears entire cart
- `createStore()`: Creates product list
- `displayCart()`: Shows cart with quantities
- `updateCart()`: Updates cart display
  - Shows "Your cart is empty" if empty
  - Shows items as "ITEM_NAME x QUANTITY (remove)"
  - Includes "Clear my cart" option at top

**Access:** http://localhost:8080/7-index.html

## 🔑 Key Concepts

### Cookies
- Small pieces of data stored in the browser
- Can have expiration dates
- Sent with every HTTP request
- Limited size (~4KB)

### Local Storage
- Stores data with no expiration date
- Shared across all tabs/windows of the same origin
- Persists after browser restart
- Larger storage capacity (~5-10MB)

### Session Storage
- Similar to Local Storage but session-scoped
- Data only available for the current tab
- Cleared when tab is closed
- Not shared between tabs

## 🛠️ Technologies Used

- **Vanilla JavaScript**: No frameworks, pure JavaScript
- **Webpack Dev Server**: Development server
- **js-cookie**: Cookie manipulation library (Task 4)
- **HTML5**: Semantic markup
- **CSS3**: Styling

## 📝 Notes

- All JavaScript code is written in vanilla JavaScript (no frameworks)
- DOM manipulation is done entirely with JavaScript
- No external dependencies except js-cookie (Task 4)
- `src/index.js` remains empty as per requirements

## 🧪 Testing

To test the differences between Local Storage and Session Storage:

1. **Local Storage (Task 5)**:
   - Add items to cart
   - Open new tab → items still there
   - Close browser → items persist

2. **Session Storage (Task 6)**:
   - Add items to cart
   - Open new tab → items NOT there
   - Close tab → items lost

## 📄 License

ISC

## 👤 Author

Holberton School Web Front End Project
