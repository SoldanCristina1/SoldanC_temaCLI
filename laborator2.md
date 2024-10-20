Laborator #02

1.

GL.Ortho(-2.0, 2.0, -2.0, 2.0, 0.0, 4.0);
Când schimbăm valoarea constantei „MatrixMode.Projection”, obiectele din perspectivă par mai mici pe măsură ce sunt mai departe, ca în viața reală(exemplu: sinele de tren). În proiecția ortogonală, obiectele rămân la fel de mari, indiferent cât de departe sunt.

3.
1. Ce este un viewport?
   Un viewport este zona din fereastră în care se afișează imaginea 3D, definind cât de mult din scena 3D este vizibil pe ecran.

1. Ce reprezintă conceptul de frames per second (FPS) în OpenGL?
   Conceptul de frames per second (FPS) reprezintă numărul de imagini afișate pe secundă, iar un FPS mai mare indică o animație mai fluidă.

1. Când este rulată metoda OnUpdateFrame()?
   Metoda OnUpdateFrame() este rulată la fiecare cadru pentru a actualiza logica aplicației, inclusiv mișcarea obiectelor și reacția la intrările utilizatorului.

1. Ce este modul imediat de randare?
   Modul imediat de randare este un mod în care formele, cum ar fi triunghiurile, sunt desenate direct folosind comenzi simple, dar este considerat ineficient pentru aplicațiile moderne.

1. Care este ultima versiune de OpenGL care acceptă modul imediat?
   Ultima versiune de OpenGL care acceptă modul imediat de randare este OpenGL 3.5.

1. Când este rulată metoda OnRenderFrame()?
   Metoda OnRenderFrame() este rulată după OnUpdateFrame() și se ocupă de desenarea efectivă a scenei pe ecran.

1. De ce trebuie să fie executată metoda OnResize() cel puțin o dată?
   Metoda OnResize() trebuie executată cel puțin o dată pentru a seta corect dimensiunea viewport-ului, în special atunci când fereastra este redimensionată.

1. Ce reprezintă parametrii metodei CreatePerspectiveFieldOfView() și care este domeniul de valori pentru aceștia?
   Parametrii metodei CreatePerspectiveFieldOfView() sunt unghiul de vedere (fieldOfView), raportul de aspect (aspectRatio), distanța minimă de vizibilitate (nearClip) și distanța maximă de vizibilitate (farClip), iar aceste valori trebuie respectate pentru a asigura o proiecție corectă.
