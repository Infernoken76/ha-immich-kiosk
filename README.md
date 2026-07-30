# ha-immich-kiosk

Home Assistant Supervisor add-on repository voor Immich Kiosk.

## Toevoegen aan Home Assistant

1. Ga in HA naar **Instellingen → Add-ons → Add-on Store**.
2. Klik rechtsboven op de drie puntjes → **Repositories**.
3. Plak de URL van deze repo en klik **Add**.
4. Ververs de store. De add-ons hieronder verschijnen in een eigen sectie.

## Add-ons

### Immich Kiosk (`immich_kiosk/`)

Wrapper rond de officiële `damongolding/immich-kiosk` Docker image.
Toont een live-updatende slideshow van een Immich-album (bv. voor een feestje),
zonder dat nieuwe foto's een herstart vereisen.

Na installatie, vul in het **Configuration**-tabblad in:
- `KIOSK_IMMICH_URL` — bv. `http://homeassistant.local:2283`
- `KIOSK_IMMICH_API_KEY` — API key uit Immich (Account Settings → API Keys)
- `KIOSK_ALBUMS` — album-ID uit de Immich album-URL

Daarna is de slideshow bereikbaar op poort `3000`, bijvoorbeeld:
`http://homeassistant.local:3000?disable_ui=true`

Gebruik die URL in een **Webpage-kaart** op je Lovelace-dashboard, of als
achtergrond-URL van een view via `.../image`.
