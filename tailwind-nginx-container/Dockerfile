FROM nginx

# Install Node.js and npm
RUN apt-get update && apt-get install -y \
  curl \
  gnupg \
  ca-certificates \
&& curl -fsSL https://deb.nodesource.com/setup_16.x | bash - \
&& apt-get install -y nodejs

# Configure Tailwind CSS
WORKDIR /var/www/html

# Install Tailwind CSS and Preline
RUN npm install -D tailwindcss
# Copy default.conf
COPY default.conf /etc/nginx/conf.d/default.conf
