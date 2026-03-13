**Use this to deal with ActionBar in gtk-rs (GTK4 in Rust) :**

```
let action_bar = gtk::ActionBar::new();

// New (btn)
let img_new = gtk::Image::from_file("src/assets/images/32_new_document.png");
let btn_new = gtk::Button::builder().build();
btn_new.set_child(Some(&img_new));
btn_new.connect_clicked(move |_| {
    // TODO: Code to refresh program
});
action_bar.pack_start(&btn_new);

// Open (btn)
let img_open = gtk::Image::from_file("src/assets/images/32_folder.png");
let btn_open = gtk::Button::builder().build();
btn_open.set_child(Some(&img_open));
btn_open.connect_clicked(move |_| {
    // TODO: Code to open project
});
action_bar.pack_start(&btn_open);

// Save (btn)
let img_save = gtk::Image::from_file("src/assets/images/32_floppy_disk.png");
let btn_save = gtk::Button::builder().build();
btn_save.set_child(Some(&img_save));
btn_save.connect_clicked(move |_| {
    // TODO: Code to save project
});
action_bar.pack_start(&btn_save);
```

**You can obtain a similary Action Bar :**

![Action Bar](https://github.com/TW2/Rustine/blob/master/gtk-rs/images/gtk-rs-action_bar.png)
