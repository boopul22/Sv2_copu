# Sayari Blog - Hindi Shayari, Quotes & Wishes

A modern React application for Hindi Shayari, Quotes, and Wishes, migrated from WordPress with Supabase as the backend database.

## 🚀 Features

- **Modern Tech Stack**: Built with Vite + React for fast development and optimal performance
- **Clean URL Structure**: Individual posts accessible at `/:slug` (e.g., `/my-shayari-title`)
- **Supabase Integration**: Robust backend with PostgreSQL database
- **Responsive Design**: Mobile-first approach with CSS Grid and Flexbox
- **Search Functionality**: Search across posts, authors, categories, and tags
- **Pagination**: "Load More" functionality for better user experience
- **Performance Optimized**: Efficient database queries and parallel data fetching

## 🛠️ Tech Stack

- **Frontend**: React 18, Vite, React Router v6
- **Backend**: Supabase (PostgreSQL)
- **Styling**: CSS3 with Grid and Flexbox
- **Language**: JavaScript/JSX

## 📁 Project Structure

```
src/
├── components/
│   ├── Header.jsx
│   └── PostCard.jsx
├── pages/
│   ├── Home.jsx
│   ├── SinglePost.jsx
│   ├── Category.jsx
│   ├── Tag.jsx
│   ├── Author.jsx
│   └── Authors.jsx
├── lib/
│   └── supabase.js
├── App.jsx
└── main.jsx
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/niraladk753/sayari-blog-react.git
cd sayari-blog-react
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env
```
Then edit `.env` with your actual Supabase credentials:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

⚠️ **Important**: See [ENVIRONMENT_VARIABLES.md](./ENVIRONMENT_VARIABLES.md) for detailed setup instructions and security best practices.

4. Start the development server:
```bash
npm run dev
```

5. Open [http://localhost:5173](http://localhost:5173) in your browser.

## 📊 Database Schema

The application uses the following Supabase tables:
- `posts` - Blog posts with content, metadata, and relationships
- `categories` - Post categories
- `tags` - Post tags
- `users` - Authors/users
- `post_categories` - Many-to-many relationship between posts and categories
- `post_tags` - Many-to-many relationship between posts and tags

## 🔧 Key Features Implemented

### URL Structure Migration
- Changed from `/post/:slug` to `/:slug` for cleaner URLs
- Proper route priority to prevent conflicts with specific routes

### Performance Optimizations
- Pagination with 12 posts per page
- Optimized database queries with field selection
- Parallel query processing using Promise.all
- Efficient loading states

### Database Fixes
- Resolved column reference issues (`author_wp_id` → `author_id`)
- Fixed foreign key relationships
- Optimized query performance

## 🚀 Deployment

### Environment Variables Setup
**⚠️ CRITICAL**: Before deploying, you MUST set up environment variables on your hosting platform.

1. **Cloudflare Pages** (Current deployment):
   - Go to your project dashboard → Settings → Environment variables
   - Add `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY`
   - See [ENVIRONMENT_VARIABLES.md](./ENVIRONMENT_VARIABLES.md) for detailed instructions

2. **Other Platforms**:
   - **Vercel**: Add environment variables in project settings
   - **Netlify**: Add in Site settings → Environment variables
   - **GitHub Pages**: Use GitHub Secrets for Actions

### Build Commands
```bash
npm run build
# Deploy dist/ folder to Netlify
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Original WordPress content and design
- Supabase for providing excellent backend services
- React and Vite communities for amazing tools

## 📞 Contact

- GitHub: [@niraladk753](https://github.com/niraladk753)
- Email: dhananjay753@gmail.com

---

**Note**: This project was migrated from a WordPress installation to provide better performance, modern development experience, and cleaner URL structure while maintaining all original content and functionality.
