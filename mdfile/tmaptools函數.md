# tmap函數

- approx_areas()
- approx_distances()
- bb()
- bb_poly()
- calc_densities()
- crop_shape()
- geocode_OSM()
- get_asp_ratio()
- get_brewer_pal()
- get_neighbours()
- map_coloring()
- palette_explorer()
- read_GPX()
- read_osm()
- rev_geocode_OSM()
- simplify_shape()

## shiny 寫法

```{r}
# in UI part:
leafletOutput("my_tmap")

# in server part
output$my_tmap = renderLeaflet({
    tm <- tm_shape(World) + 
      tm_polygons("HPI", legend.title = "Happy Planet Index")
    tmap_leaflet(tm)
})
```
