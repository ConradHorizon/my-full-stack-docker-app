FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
# Add the build step
RUN npm run build
# Install a small server to host the build
RUN npm install -g serve
EXPOSE 3000
# Serve the 'dist' or 'build' folder (check your project, usually 'dist' for Vite or 'build' for CRA)
CMD ["serve", "-s", "dist", "-l", "3000"]

# Force Redo

