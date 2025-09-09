# IntranetAI

AI-powered intranet solution for modern organizations.

## 🚀 Quick Start

1. Clone the repository:
   ```bash
   git clone https://github.com/ketipotova/intranetai.git
   cd intranetai
   ```

2. Set up environment variables:
   ```bash
   cp .env .env.local
   # Edit .env.local with your actual API keys
   ```

3. Install dependencies and start development:
   ```bash
   # For Node.js projects
   npm install
   npm run dev
   
   # For Python projects
   pip install -r requirements.txt
   python manage.py runserver
   ```

## 🏗️ Infrastructure

This project is set up with:

- **Version Control**: GitHub repository at `https://github.com/ketipotova/intranetai`
- **Frontend Deployment**: Vercel (auto-deploys from main branch)
- **Backend Deployment**: Railway (requires manual setup)
- **CI/CD**: GitHub Actions with automated testing and deployment

## 🔧 Deployment Setup

### Vercel Setup ✅
Already configured and deployed. Production URL: https://intranetai-efgyuozr7-ketevans-projects.vercel.app

### Railway Setup 🚧
To complete Railway setup:

1. Login to Railway:
   ```bash
   railway login
   ```

2. Initialize project:
   ```bash
   railway init
   ```

3. Deploy:
   ```bash
   railway up
   ```

### GitHub Actions Secrets

Add these secrets to your GitHub repository for full CI/CD functionality:

- `VERCEL_TOKEN` - Your Vercel account token
- `VERCEL_ORG_ID` - Your Vercel organization ID
- `VERCEL_PROJECT_ID` - Your Vercel project ID
- `RAILWAY_TOKEN` - Your Railway project token
- `RAILWAY_SERVICE` - Your Railway service name

## 🤝 Contributing

1. Create a feature branch from `main`
2. Make your changes
3. Ensure tests pass
4. Create a pull request

Pull requests will automatically:
- Run tests
- Deploy preview environments
- Deploy to production on merge to main

## 📝 Environment Variables

Create a `.env.local` file with:

```env
SUPABASE_ANON_KEY=your_supabase_anon_key_here
CLAUDE_API_KEY=your_claude_api_key_here
```

## 🔄 CI/CD Pipeline

- **On PR**: Runs tests and deploys preview
- **On merge to main**: Runs tests and deploys to production
- **Dependabot**: Weekly dependency updates