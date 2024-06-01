# ByteQuest Project

## Overview

This project is a simple Next.js application that includes a React component to display item cards. Each item card shows an image, title, and price of a product.

## Features

- Next.js for server-side rendering and optimized performance.
- TypeScript for type safety and improved developer experience.
- React for building the user interface.
- Tailwind CSS for styling the components.
- `Image` component from `next/image` for optimized image loading.


## Component Details

### ItemCard Component

The `ItemCard` component is a reusable component that displays an item with its image, title, and price. The component uses the `next/image` component for optimized image loading.

#### Props

- `id`: `string` - Unique identifier for the item.
- `image`: `string` - URL of the item's image.
- `title`: `string` - Title of the item.
- `price`: `number` - Price of the item.
- `category`: `string` - Category of the item (not used in the component, but available for future use).

#### Example Usage

```tsx
import React from 'react';
import ItemCard from './components/ItemCard';

const items = [
  {
    id: '1',
    image: '/images/item1.jpg',
    title: 'Item 1',
    price: 100,
    category: 'Category 1',
  },
  {
    id: '2',
    image: '/images/item2.jpg',
    title: 'Item 2',
    price: 200,
    category: 'Category 2',
  },
];

const HomePage = () => {
  return (
    <div className="container mx-auto">
      <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
        {items.map((item) => (
          <ItemCard
            key={item.id}
            id={item.id}
            image={item.image}
            title={item.title}
            price={item.price}
            category={item.category}
          />
        ))}
      </div>
    </div>
  );
};

export default HomePage;
```

Installation:
  - step_1: |
      Clone the repository:
      ```bash
      git clone https://github.com/yourusername/item-card-project.git
      ```
  - step_2: |
      Navigate to the project directory:
      ```bash
      cd item-card-project
      ```
  - step_3: |
      Install the dependencies:
      ```bash
      npm install
      ```
  - step_4: |
      Run the development server:
      ```bash
      npm run dev
      ```
  - step_5: "Open your browser and navigate to `http://localhost:3000` to see the application in action."

Deployment:
  - build: |
      To build the project for production, run:
      ```bash
      npm run build
      ```
  - start: |
      To start the production server, run:
      ```bash
      npm start
      ```

license: "This project is licensed under the MIT License."

acknowledgements:
  - Next.js: "https://nextjs.org/"
  - React: "https://reactjs.org/"
  - TypeScript: "https://www.typescriptlang.org/"
  - Tailwind CSS: "https://tailwindcss.com/"
  - Vercel: "https://vercel.com/"

