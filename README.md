# Dynamic Directory Template

A flexible, responsive directory website template that can be adapted for various use cases such as business listings, restaurant directories, service provider catalogs, and more.

## 🚀 Demo
[Include your demo link here]

## ✨ Features

- 🔍 Real-time search functionality
- 📂 Category filtering
- 🔄 Dynamic sorting (name/rating)
- 📱 Fully responsive design
- 🎨 Clean, modern UI with card-based layout
- ⚡ Lightweight and performant
- 🛠 Easy to customize and extend

## 🔧 Technologies Used

- HTML5
- CSS3
- Alpine.js (v3.13.5) - for reactive data handling
- Lodash (v4.17.21) - for utility functions

## 📦 Installation

1. Clone the repository:
```bash
git clone [your-repository-url]
cd directory-template
```

2. Open `index.html` in your web browser

No build process required! The template uses CDN links for dependencies.

## 🔍 Program Structure

### HTML Structure
```
├── Header
│   └── Title and description
├── Main Content
│   ├── Search Bar
│   ├── Filters Section
│   │   ├── Category Filter
│   │   └── Sort Options
│   └── Directory Grid
│       └── Directory Items
```

### Data Model
```javascript
{
    items: [
        {
            name: string,
            category: string,
            description: string,
            rating: number,
            image: string
        }
    ]
}
```

### Key Components

#### 1. Alpine.js State Management
```javascript
x-data={
    searchQuery: '',      // Search input value
    selectedCategory: '', // Selected category filter
    selectedSort: 'name', // Current sort criterion
    items: [],           // Directory items array
    filteredItems()      // Computed property for filtered results
}
```

#### 2. Search Functionality
- Real-time filtering based on item names
- Case-insensitive search
- Instant results updating

#### 3. Filter System
- Category-based filtering
- Maintains state with Alpine.js
- Easily extensible for additional filter criteria

#### 4. Sort System
- Currently supports sorting by:
  - Name (alphabetical)
  - Rating (numerical)
- Extensible sort logic in the `filteredItems` computed property

## 🎨 Customization

### Adding New Categories
1. Update the select options in the HTML:
```html
<select x-model="selectedCategory">
    <option value="">All Categories</option>
    <option>Your New Category</option>
</select>
```

### Adding New Sort Options
1. Add new option to the sort select:
```html
<select x-model="selectedSort">
    <option value="name">Name</option>
    <option value="rating">Rating</option>
    <option value="yourNewSort">Your New Sort</option>
</select>
```

2. Update the sort logic in `filteredItems`:
```javascript
if (this.selectedSort === 'yourNewSort') {
    return a.yourProperty - b.yourProperty;
}
```

### Styling
- The template uses a modular CSS structure
- Key CSS classes:
  - `.directory-grid`: Main grid container
  - `.directory-item`: Individual listing cards
  - `.item-content`: Content within cards
  - `.search-bar`: Search input container
  - `.filters`: Filter section styling

## 📱 Responsive Behavior

- Mobile-first design approach
- Breakpoints:
  - Mobile: < 768px (single column)
  - Tablet & Desktop: ≥ 768px (multi-column grid)
- Fluid typography and spacing
- Responsive images with object-fit

## 🔄 Performance Considerations

- Uses CSS Grid for efficient layouts
- Minimal JavaScript footprint
- Optimized Alpine.js reactivity
- Lazy loading ready for images
- No unnecessary re-renders

## 🎯 Future Enhancements

- [ ] Add pagination/infinite scroll
- [ ] Implement advanced filtering
- [ ] Add detail view modal
- [ ] Include map integration
- [ ] Add favorite/bookmark functionality
- [ ] Implement dark mode
- [ ] Add loading states
- [ ] Include animation effects

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

[Include your license here]

## 👏 Acknowledgments

- Alpine.js team for the reactive framework
- Lodash team for utility functions
