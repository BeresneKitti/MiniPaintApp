Hallgató

Béresné Hanák Kitti M0861K

Program leírása
  A projekt egy egyszerű rajzprogram, Tkinter grafikus felülettel.
  A felhasználó szabadkézzel rajzolhat, színt és ecsetméretet választhat, törölheti a vásznat, véletlenszerű stílust kérhet, valamint JPG vagy PNG formátumba mentheti a rajzot.

Fájlszerkezet
  main.py          # Program indítása
  app.py           # Grafikus alkalmazás (Tkinter)
  bhk_modul.py     # Saját modul
  README.md        # Leírás

Modulok és függvények
  main.py
    A program belépési pontja.
    Létrehozza a Tkinter főablakot és elindítja a BHKMiniPaintApp alkalmazást.

  app.py
    A fő grafikus alkalmazás.
    Osztály:
      BHKMiniPaintApp – a teljes rajzprogram működését megvalósítja.
    Függvények:
      create_widgets()
      create_events()
      on_canvas_press()
      on_canvas_drag()
      on_canvas_release()
      on_clear_canvas()
      on_random_color()
      on_random_style()
      on_save_image()
      on_exit()
      update_status()
      update_header_date()
    A rajzolás a Tkinter vászonra és egy háttérben futó PIL képre egyszerre történik, így mentéskor csak a vászon tartalma kerül a JPG/PNG fájlba.

bhk_modul.py
  Saját modul BHK monogrammal.
  Osztály:
    BHKDrawingInfo – tárolja a rajzolás adatait (vonalak száma, kezdési idő, utolsó rajzolási idő).
  Függvények:
    bhk_register_stroke() – saját függvény monogrammal
    bhk_status_text()
    bhk_default_colors()
    Grafikai modul
    Tkinter (Canvas, Button, Scale, Combobox)
    Pillow (Image, ImageDraw) – a rajz JPG/PNG mentéséhez
  Eseménykezelés
    <Button-1> – rajzolás kezdete
    <B1-Motion> – rajzolás mozgás közben
    <ButtonRelease-1> – rajzolás vége
    <Escape> – kilépés
