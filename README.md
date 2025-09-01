# 📂 Project Structure

All source code resides inside the `src` folder (you can keep tests separately in a `tests` folder).  
Here’s a quick overview of the structure:

- **`config/`** → Handles project configurations and setups for libraries/modules.  
  - Example: Setting up `dotenv` to manage environment variables (`server-config.js`).  
  - Example: Configuring a logging library for structured and meaningful logs.  

- **`routes/`** → Defines application routes, along with their middlewares and controllers.  

- **`middlewares/`** → Intercepts incoming requests for validations, authentication, etc.  

- **`controllers/`** → Acts as the last middleware.  
  - Accepts incoming requests.  
  - Calls the business logic (services).  
  - Structures and sends back API responses.  

- **`repositories/`** → Responsible for database interactions.  
  - Raw queries or ORM-based queries live here.  

- **`services/`** → Contains business logic.  
  - Talks to repositories for database operations.  

- **`utils/`** → Utility/helper functions, custom error classes, etc.  

---

# ⚙️ Setup Instructions

1. **Clone or download** this template and open it in your preferred editor.  

2. **Install dependencies**  
   ```bash
   npm install
Create a .env file in the root directory and add your environment variables:

env
Copy code
PORT=3000
Initialize Sequelize (inside the src folder):

bash
Copy code
npx sequelize init
This will generate migrations/, seeders/, and a config.json inside config/.

Configure your database

For development, set username, password, and dialect (e.g., mysql, mariadb).

For test/production, also update the host with your hosted DB URL.

Start the server

bash
Copy code
npm run dev
