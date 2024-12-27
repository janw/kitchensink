
FROM docker.io/ptr727/plexcleaner:alpine AS cleaner

FROM ghcr.io/linuxserver/sabnzbd:4.4.1

# hadolint ignore=DL3018
RUN set -e; \
    apk add --no-cache \
        dotnet8-runtime \
        ffmpeg \
        handbrake \
        mediainfo \
        mkvtoolnix \
    ;


COPY --from=cleaner /PlexCleaner /PlexCleaner
