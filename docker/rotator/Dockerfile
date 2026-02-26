# Using lightweight alipine image
FROM node:20-alpine

# Setting the working directory
WORKDIR /usr/src/app

COPY package.json package-lock.json ./

# Installing application dependencies
RUN npm ci --omit=dev || npm install --omit=dev

# Copy the rest of the app
COPY . .

# Enabling the production optimization
ENV NODE_ENV=production

# Expose port 3000
EXPOSE 3000

# Run the application
CMD ["npm", "start"]