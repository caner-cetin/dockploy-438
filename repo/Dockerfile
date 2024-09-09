FROM busybox:1.35.0-uclibc as busybox
# Stage 2: Create the final distroless image
FROM gcr.io/distroless/base-debian12
WORKDIR /var/www/html
COPY --from=busybox /bin/ /bin/
CMD ["/bin/sh", "-c", "while true; do sleep 3600; done"]
