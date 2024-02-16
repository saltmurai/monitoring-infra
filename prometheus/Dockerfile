# Use the official Prometheus image as the base image
FROM prom/prometheus:v2.33.5

# Set the working directory inside the container
WORKDIR /etc/prometheus

# Copy your Prometheus configuration file into the container
# Make sure you have a prometheus.yml configuration file in your context
COPY config/prometheus.yml /etc/prometheus/prometheus.yml

# Expose the Prometheus default port
EXPOSE 9090

# Specify the command to run Prometheus
# --config.file specifies the path to the configuration file
# --storage.tsdb.path specifies the path for storing time series data
# --web.enable-lifecycle enables certain web operations such as changing the configuration file
CMD ["--config.file=/etc/prometheus/prometheus.yml", "--storage.tsdb.path=/prometheus", "--web.enable-lifecycle"]
