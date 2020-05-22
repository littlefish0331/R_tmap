# tmap函數

- tmap_options(bg.color, legend.text.color)
- tmap_style(style, bg.color, space.color, inner.margins, earth.boundary)
- tmap_mode(mode)
- tm_basemap(server, alpha, group)
- tm_view(alpha, basemaps)
- tm_tiles(server, alpha, group)
- tm_raster(col, breaks, palette, legend.show, title)
- tm_shape(shp, is.master, projection)
- tm_borders(col, lwd, alpha)
- tm_text(text, size, col, root)
- tm_symbols(col, size, scale)
- tm_dots(col, group)
- tm_lines(col, lwd, scale, legend.lwd.show)
- tm_bubbles(size, col, border.col, border.alpha, breaks, palette, title.size, title.col, id, popup.vars)
- tm_polygons(col, alpha, border.col, border.alpha, group, palette, contrast, convert2density, title, id, colorNULL, colorNA, breaks, showNA)
- tm_fill(col, palette, title)
- tm_grid(projection, labels.size, lwd)
- tm_compass(position, color.light, size)
- tm_scale_bar(position)
- tm_credits(text, position)
- tm_legend(show, position, frame, bg.color, frame, outside)
- tm_layout(title, title.position, title.size, bg.color, inner.margins, legend.show, legend.position, frame, frame.lwd)
- tm_facets(by, ncol, nrow, free.coords)
- tmap_arrange(ncol, nrow, sync)
- tmap_options_diff()
- tmap_options_reset()
- tmap_save(tm, filename, width, height, scale, dpi, asp, outer.margins, insets_tm, insets_vp)
- qtm(shp, fill, fill.pallete, symbols.col, symbols.size, raster.saturation, raster.alpha)
- tmap_tip()
- tmap_format(format, inner.margins, frame, frame.lwd)
- tmap_format_add(name)

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
