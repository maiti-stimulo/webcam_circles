# Circle detection from online webcam images


Links consultats

http://docs.opencv.org/2.4/doc/tutorials/imgproc/imgtrans/hough_circle/hough_circle.html

https://ca.wikipedia.org/wiki/Transformada_de_Hough



La Transformada de Hough va ser inventada inicialment per a l'anàlisi de la Càmera de bombolles. Hough el 1962, va inventar la transformació per a una aplicació en la detecció de les rutes de partícules subatòmiques passant per un camp de visió.

La transformada original de Hough va ser dissenyada per detectar línies rectes i corbes, aquest mètode s'utilitzava només si es coneixen les equacions analítiques de les línies o corbes de l'objecte. Més tard, es va descriure la transformada generalitzada de Hough que podia trobar objectes encara que no es coneguès l'equació analítica.

#Tècnica
és una tècnica que s’utilitza en imatges que permet detectar certes figures geomètriques dins d'una imatge. La idea  es basa en transformar punts d’una imatge en paràmetres que puguin ser detectats com a rectes, cercles I polininomis. 
Inicialment estava pensada per a la detecció de rectes, el detectar cercles ha fet més complexe el càlcul, ja que hem passat d’una equaciò Y=mX+b a una de segon grau R=sqrt((x-a)²+(y-b)²), això dificulta l’algorisme, ja que donarà lloc a un espai de paràmetres de tres dimensions, amb cel·les en forma de cub i acumuladors (que són subdivisions de l'espai paramètric - de la forma f(r,x,y))

#Paràmetres que defineixen la funció de detecció de cercles.

HoughCircles(InputArray image, OutputArray circles, int method, double dp, double minDist, double param1=100, double param2=100, int minRadius=0, int maxRadius=0 )

src_gray: imatge escala de grisos
circles: Matriu de tres valors X, Y I Radi per cada cercle detectat. 
CV_HOUGH_GRADIENT: métode de detecció
dp = Es la inversa del rati de la ressolució 
min_dist = Distància minima entre cercles detectats 
param_1 = Filtra imatges que no estan dins del parametres desitjats 
param_2 = Detecció dels cercles. 
min_radius =  Radi minim a detectar. 
max_radius = Radi màxim a detectar




