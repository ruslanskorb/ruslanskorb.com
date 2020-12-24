FROM node:9.4.0

# Create an unprivileged user
RUN useradd --user-group --create-home --shell /bin/false ruslanskorb && npm install --global npm@6.4.1

# Define environment variables
ENV HOME=/home/ruslanskorb

# Copy the packaging files into the app directory and set permissions for reading
COPY package.json $HOME/ruslanskorb-node/
COPY client $HOME/ruslanskorb-node/client
COPY gulpfile.coffee $HOME/ruslanskorb-node/
RUN chown -R ruslanskorb:ruslanskorb $HOME/*

# Set current user
USER ruslanskorb

# Set an app directory
WORKDIR $HOME/ruslanskorb-node

# Install app dependencies
RUN npm install && npm cache verify

# Set current user
USER root

# Copy the source files into the app directory and set permissions for reading
COPY . $HOME/ruslanskorb-node
RUN chown -R ruslanskorb:ruslanskorb $HOME/*

# Set current user
USER ruslanskorb

# Expose a port
EXPOSE 8080

# Run a server
CMD ["node_modules/.bin/coffee", "server/app.coffee"]
