**Using this in gtk-rs to dealing with Notebook (GTK4 with Rust)**

```
let notebook = gtk::Notebook::builder()
    .hexpand(true)
    .build();

// Page 1
let container_001 = gtk::Box::new(gtk::Orientation::Vertical, 0);
let label_001 = gtk::Label::new(None);
label_001.set_label("Page 1");

// Page 2
let container_002 = gtk::Box::new(gtk::Orientation::Vertical, 0);
let label_002 = gtk::Label::new(None);
label_002.set_label("Page 2");

// Page 3
let container_003 = gtk::Box::new(gtk::Orientation::Vertical, 0);
let label_003 = gtk::Label::new(None);
label_003.set_label("Page 3");

notebook.append_page(&container_001, Some(&label_001));
notebook.append_page(&container_002, Some(&label_002));
notebook.append_page(&container_003, Some(&label_003));
```
