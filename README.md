# Balls and their Admirers

Et C-program der simulerer en samling farvede bolde, som bevæger sig rundt på skærmen og følger hinanden.  
Hver bold får tilfældigt tildelt farve, position, hastighed og størrelse ved opstart.  
Visualiseringen håndteres ved hjælp af **Raylib**.

---

## Use
```bash
gcc .\Balls\Balls.c -o .\Balls\Balls.exe -I"raylib-5.5_win64_mingw-w64\include" -L"raylib-5.5_win64_mingw-w64\lib" -lraylib -lopengl32 -lgdi32 -lwinmm
.\Balls\Balls.exe
```

The program:

- Initialiserer 100 bolde med tilfældige positioner, hastigheder og farver.
- Hver bold vælger tilfældigt en anden bold, som den følger.
- Opdaterer boldenes bevægelse i realtid (60 FPS).
- Tegner alle bolde løbende i et Raylib-vindue.

Files:

- Balls.c – Hovedprogrammet med logik, initialisering, og tegning
- raylib.h – Bibliotek brugt til grafik og animation
- libraylib.a – Linket statisk Raylib-bibliotek

Funcitons:

- init_balls_random() – Initialiserer alle bolde med tilfældige værdier
- update_vel_for_following() – Justerer hastighed så bolden følger en anden
- update_pos() – Opdaterer boldens position baseret på dens hastighed
- draw_ball() – Tegner en enkelt bold i vinduet
- update_elements() – Opdaterer og tegner alle bolde i hver frame
