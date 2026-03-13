**Use this to draw on a drawing area in gtk-rs (GTK4 in Rust) :**

```
let drawing_area = gtk::DrawingArea::new();

// Set the size of the drawing area.
drawing_area.set_width_request(400);
drawing_area.set_height_request(400);

// Set the drawing function.
DrawingAreaExtManual::set_draw_func(&drawing_area, move |_, cr, w, h| {
    let r = w as f64 / 2.0 - 1.0;

    cr.set_source_rgb(0.5, 0.5, 0.5);
    cr.arc(w as f64 / 2.0, h as f64 / 2.0, r, 0.0, 2.0 * PI);
    cr.fill().unwrap();

    cr.set_source_rgb(0.3, 0.8, 1.0);
    cr.set_line_width(1.0);
    cr.arc(w as f64 / 2.0, h as f64 / 2.0, r, 0.0, 2.0 * PI);
    cr.stroke().unwrap();
});
```
