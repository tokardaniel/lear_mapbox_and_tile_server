## Szerver oldali tile server elindítása docker-ben

```bash
docker run --rm -it -v .:/data -p 8080:8080 maptiler/tileserver-gl:latest --file hungary.mbtiles
```

## OSM adatok letöltése Magyarország területére

```bash
docker run -e JAVA_TOOL_OPTIONS="-Xmx4g" -v ./data:/data ghcr.io/onthegomap/planetiler:latest --download --area=hungary --output=/data/hungary.mbtiles
```
