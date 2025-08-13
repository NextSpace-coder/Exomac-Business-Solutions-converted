# Business Solutions Platform

A modern React-based business platform template designed for professional services and business growth solutions.

## Features

- **Modern Design**: Clean and professional UI/UX design
- **React 18**: Built with the latest React features
- **Bootstrap 5**: Responsive design framework
- **Supabase Integration**: Backend-as-a-Service for data management
- **Multiple Pages**: Home, About, Services, Portfolio, Contact, and Blog
- **Animations**: AOS (Animate On Scroll) animations
- **Mobile Responsive**: Optimized for all devices
- **SEO Optimized**: Meta tags and structured data
- **Contact Forms**: Integrated contact and project forms
- **Portfolio Gallery**: Showcase your work and projects
- **Team Section**: Display team members
- **Testimonials**: Customer reviews and feedback
- **Newsletter**: Email subscription integration

## Quick Start

1. **Clone the repository**
   ```bash
   git clone [repository-url]
   cd business-solutions-platform
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   Edit `.env` with your Supabase credentials:
   ```
   REACT_APP_SUPABASE_URL=https://your-project.supabase.co
   REACT_APP_SUPABASE_ANON_KEY=your-anon-key
   ```

4. **Start development server**
   ```bash
   npm start
   ```

5. **Build for production**
   ```bash
   npm run build
   ```

## Supabase Setup

1. Create a new project at [supabase.com](https://supabase.com)
2. Get your project URL and anonymous key from Settings > API
3. Update the environment variables in `.env`

### Database Schema Examples

```sql
-- Contact submissions table
CREATE TABLE contacts (
  id BIGSERIAL PRIMARY KEY,
  name TEXT NOT NULL,
  email TEXT NOT NULL,
  message TEXT NOT NULL,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- Newsletter subscriptions table
CREATE TABLE newsletter (
  id BIGSERIAL PRIMARY KEY,
  email TEXT UNIQUE NOT NULL,
  subscribed_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);
```

## Project Structure

```
src/
├── components/          # Reusable UI components
├── container/          # Page containers and sections
├── data/              # Static data and content
├── pages/             # Page components
├── assets/            # Images, styles, and static assets
├── lib/               # Utility functions and Supabase config
└── hooks/             # Custom React hooks
```

## Available Scripts

- `npm start` - Start development server (Port 3008)
- `npm run build` - Build for production
- `npm test` - Run tests
- `npm run lint` - Run ESLint
- `npm run lint:fix` - Fix ESLint issues

## Pages Included

- **Home** - Main landing page with hero section
- **About** - Company information and values
- **Services** - Service offerings and capabilities
- **Portfolio** - Project showcase and gallery
- **Team** - Team member profiles
- **Blog** - News and articles
- **Contact** - Contact information and forms

## Customization

### Styling
- Modify SCSS files in `src/assets/scss/`
- Update color variables in `_root.scss`
- Customize components in their respective SCSS files

### Content
- Update data files in `src/data/` directory
- Modify component content in their respective files
- Replace images in `public/images/` directory

### Branding
- Replace logo files in `public/images/logo/`
- Update favicon in `public/images/favicon.png`
- Modify site title and description in `public/index.html`

## Dependencies

### Core
- React 18.2.0
- React Router DOM 6.3.0
- Bootstrap 5.2.0

### Supabase & Data
- @supabase/supabase-js
- react-query

### UI Components & Animations
- AOS (Animate On Scroll)
- Swiper (Sliders)
- React Bootstrap
- React Modal Video
- React CountUp

### Forms & Interactions
- React Hook Form
- React Helmet (SEO)
- Typewriter Effect

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This project is licensed under the MIT License.

## Support

For support and questions, please contact the development team or create an issue in the repository.
