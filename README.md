# thasha-assets

Public brand assets for the **Sadhaka-Yantra** publishing pipeline, organised as a content
taxonomy:

    <category>/<topic>/<platform>/cover.png     header (platform-optimal dimensions)
    <category>/<topic>/<platform>/footer.png    article sign-off banner (4:1, per-platform width)

Slugged, variable-depth topic paths — e.g. `educational/mulesoft`, `spiritual/gods/shiva`.
`topics.yaml` maps each topic to its display name + footer CTA link.

Consumed via raw URLs, e.g.
`https://raw.githubusercontent.com/shakarbisetty/thasha-assets/main/educational/mulesoft/devto/cover.png`.

## Updating assets

High-res masters live **locally** (private) in `~/Documents/assets/Original/<topic>/{cover,footer}.png`.
To regenerate a topic's assets for every platform:

    python -m scripts.update_topic_assets --topic educational/mulesoft
    # then: git add -A && git commit -m "assets: update educational/mulesoft" && git push
