FROM node:20

WORKDIR /app

# Optimisation du cache Docker : dependances en premier
COPY package.json yarn.lock ./
RUN yarn install --frozen-lockfile

# Copie du code source
COPY . .

# Port de Vite
EXPOSE 5173

# Demarrage de Vite en ecoutant sur toutes les interfaces (0.0.0.0)
CMD ["yarn", "dev", "--host"]
