Tema 03

1. Care este ordinea de desenare a vertexurilor pentru aceste metode(orar sau anti-orar)? Desenați axele de coordonate din aplicația-template folosind un singur apel GL.Begin().
   Ordinea este anti-orar pentru triunghiuri, TriangleFan și TriangleStrip în OpenGL.

///ImmediateMode.cs

    private void DrawAxes() {

     //GL.LineWidth(3.0f);

     // Desenează axa Ox (cu roșu).
     GL.Begin(PrimitiveType.Lines);
     GL.Color3(Color.Red);
     GL.Vertex3(0, 0, 0);
     GL.Vertex3(XYZ_SIZE, 0, 0);


     // Desenează axa Oy (cu galben).
     GL.Color3(Color.Yellow);
     GL.Vertex3(0, 0, 0);
     GL.Vertex3(0, XYZ_SIZE, 0); ;


     // Desenează axa Oz (cu verde).
     GL.Color3(Color.Green);
     GL.Vertex3(0, 0, 0);
     GL.Vertex3(0, 0, XYZ_SIZE);
     GL.End();

}

2. Ce este anti-aliasing? Prezentați această tehnică pe scurt.
   Anti-aliasing este o tehnică folosită în grafică pentru a face marginile obiectelor să arate mai netede. Anti-aliasing îmbunătățește aspectul marginilor prin amestecarea culorilor pixelilor de lângă margine. În loc să folosim un singur pixel, tehnica ia mai multe măsurători din jurul marginii și combină culorile pentru a obține un aspect mai neted. Anti-aliasing ajută la crearea unor imagini mai frumoase și mai plăcute.

3. Care este efectul rulării comenzii GL.LineWidth(float)? Dar pentru GL.PointSize(float)? Funcționează în interiorul unei zone GL.Begin()?
   • GL.LineWidth(float) ajustează grosimea liniilor pe care le desenezi, permițându-ți să creezi linii mai subțiri sau mai groase, în funcție de valoarea dată.
   • GL.PointSize(float), pe de altă parte, modifică dimensiunea punctelor desenate, astfel încât să fie mai mari sau mai mici.
   Ambele comenzi trebuie apelate înainte de GL.Begin() și își vor aplica efectul asupra elementelor desenate între GL.Begin() și GL.End().

4. Care este efectul utilizării directivei LineLoop atunci când desenate segmente de dreaptă multiple în OpenGL?
   LineLoop leagă toate punctele desenate într-un ciclu, adică, după ce desenezi ultima linie, se va trasa o linie înapoi la primul punct, formând un poligon închis.

• Care este efectul utilizării directivei LineStrip atunci cânddesenate segmente de dreaptă multiple în OpenGL?
LineStrip conectează punctele desenate cu linii, dar nu se închide automat; doar primele și ultimele puncte rămân separate.
• Care este efectul utilizării directivei TriangleFan atunci când desenate segmente de dreaptă multiple în OpenGL?
TriangleFan începe cu un punct central și leagă fiecare punct din listă cu acesta, formând triunghiuri ce se radiază din centrul ales, util pentru a crea forme circulare.
• Care este efectul utilizării directivei TriangleStrip atunci când desenate segmente de dreaptă multiple în OpenGL?
TriangleStrip folosește un set de puncte pentru a crea triunghiuri adiacente, fiecare triunghi partajând două vârfuri cu triunghiul anterior, ceea ce permite desenarea unor forme complexe cu mai puține puncte.

6. Urmăriți aplicația „shapes.exe” din tutorii OpenGL Nate Robbins.De ce este importantă utilizarea de culori diferite (în gradient sau culori selectate per suprafață) în desenarea obiectelor 3D? Care este avantajul?
   Utilizarea culorilor diferite în desenarea obiectelor 3D este importantă pentru a oferi profunzime și detalii vizuale, făcând obiectele să pară mai realiste. Culorile variate ajută la evidențierea formelor și contururilor, ceea ce îmbunătățește percepția vizuală a structurii obiectului. Gradientele pot sugera iluminarea și umbrele, adăugând un efect de volum și contribuind la o experiență mai captivantă pentru utilizator. Avantajul principal este că un obiect colorat corespunzător captează atenția și poate transmite informații despre materialele și texturile sale, îmbunătățind astfel interacțiunea și înțelegerea scenei 3D.

7. Ce reprezintă un gradient de culoare? Cum se obține acesta în OpenGL?
   Un gradient de culoare reprezintă o tranziție treptată între două sau mai multe culori. Spre exemplu, dacă ne gândim la o picatura de cerneală pusă în apă, aceasta se "împrăștie" treptat.

   10.Ce efect are utilizarea unei culori diferite pentru fiecare vertex atunci când desenați o linie sau un triunghi în modul strip?
   Când atribuim o culoare diferită fiecărui vârf într-un triunghi sau o linie desenată în modul strip, OpenGL realizează un gradient de culoare între aceste vârfuri. Practic, culorile se amestecă treptat de la un vârf la altul, generând o tranziție vizuală între ele.
