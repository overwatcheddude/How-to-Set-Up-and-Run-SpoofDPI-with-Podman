# Clone the SpoofDPI repository from GitHub
git clone https://github.com/xvzc/SpoofDPI

# Navigate into the SpoofDPI directory
cd SpoofDPI/

# Build the SpoofDPI container image with Podman
podman build -t spoofdpi .

# Run the SpoofDPI container, forwarding port 8080 and setting up DNS-over-HTTPS (DoH)
podman run -p 8080:8080 spoofdpi -dns-addr 1.1.1.1 -enable-doh -window-size 1
