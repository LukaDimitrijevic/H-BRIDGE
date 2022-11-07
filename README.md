# H BRIDGE

###  Kontrolisanje dc motora preko h mosta u cilju konstruisanja pokretnog vozila

##### http://petnica.rs/

```

Kreatori projekta:
        <-Stefan Stojanović->
        Git hub: StefanCaja027
        G-mail: cajkicajkic@gmail.com

        <-Luka Dimitrijević->
        Git hub:luka.dimitrijevic@prvabeogim.edu.rs
        G-mail:LukaDimitrijevic

        <-Lazar Avramović->
        Git hub:LazarAvramovicDSP
        G-mail:cicangaming@gmail.com

```
## Tok rada i poenta projekta
Sama izrada projekta se sastojala iz 3 dela:
    1. Povezivanja šeme i kola sa arduinom;
    2. Pisanje koda u Arduino interfejsu i izveštaja u Git habu;
    3. Modeliranje i dizajniranje u fjužn 360 i 3D štampa crtanih delova iz fjužna.

Glavna svrha ovog projekta je bolje razumevanje h mosta i MOSFET transistora

Sekundarni cilj ovog projekta je konstruisanje pokretnog vozila

Za most su korišćenji MOSFET-ovi, a za pokretanje motora su korišćene 2 baterije od 9 V paralelno vezane. Točkovi auta i držači za zadnju osovinu su izrađeni na 3D štampaču, a šasija je izražena ručno.

S radom je početo 01.09.2022. i trajalo je do 08.09.2022.



```


Eng:
# Controling dc motors via h bridge with goal of making moving vehicle

### In this project, the movement of a car based on the H bridge will be shown, whose motors are powered by a 9 V battery, and with the help of an arduino and a joystick, the movement of the car is controlled.

##### http://petnica.rs/

```

Project creators:
        <-Stefan Stojanovic->
        Github acc:StefanCaja027
        G-mail:cajkicajkic@gmail.com

        <-Luka Dimitrijević->
        Github acc:LukaDimitrijevic
        G-mail:luka.dimitrijevic@prvabeogim.edu.rs

        <-Lazar Avramović->
        Github acc: LazarAvramovicDSP
        G-mail: cicangaming@gmail.com

```
## Work flow and project point
The creation of the project itself consisted of 3 parts:
    1. Schematic and circuit connections with arduino;
    2. Writing code in Arduino interface and reports in Git hub;
    3. Modeling and designing in fusion 360 and 3D printing of drawn parts from fusion.

The main purpose of this project is better undersanding of H bridge and MOSFET transistors

Side goal is to make moving vehicle


MOSFETs were used for the bridge, and 2 9 V batteries connected in parallel were used to start the motor. The wheels of the car and the brackets for the rear axle are made on a 3D printer, and the chassis is expressed by hand.

Work began on September 1, 2022. and lasted until September 8, 2022.


```

```
- # Korišćeni hardver i materijali:
```
- 1x Arduino uno;
- 4x DC motora (2 kao osovinski) od 12 V;
- 2x Duracell baterije od 9 V;
- 8x otpornik 1kΩ (po 4 za jedan H most);
- 4x IRF3415 N kanalnih MOSFET tranzistora;
- 4x IRF5305 P kanalnih MOSFET tranzistora;
- 1x džojstik;
- 3x odsečaka protoploče;
- džamperi;
- 4x točka od 3D filamenta;
- 2x držača od 3D filamenta;
- šasija od stiropora;
- ekseri;

-Hardware

Koristeći prekidačku osobinu tranzistora konstruišemo kolkonfiguraciju koje će kontrolisati smer protoka jednosmerne struje kroz kolo, pa i kroz sam motor.

//šema h mosta

Kontrola tranzistora vrši se preko Arduino uno mikrokontrolera
Kontrola samog arduino PWM-a je trebala biti bežična, ali usred manjka vremena joystick koji smo koristili za kontrolu ipak je ostao povezan za konstrukciju kablom od pola metra
Za izvor napajanja izabrane su dve baterije od 9V koje su u paralelnoj vezi
Motore koje smo pokretali bili su standardni dc motori od 12v

//slika proto kola

-Konstrukcija

Sama konstrukcija je bila izazovan deo projekta

Većinu elemenata koji interaguju sa motorima su 3D odštampani
//slika motota u konstrukciji

Sam dizajn točkova i čaura za motore urađen je u autodesk fusion 360 software-u
//slika iz fusiona

Šasija je konstruisana tvrdim stiroporom

# Software

Software nije bio komplikovan
Regulisanje protoka struje tranzistora regulisao se PWM-om koji je arduino slao u gate-ove
Takođe treba regulisati impute koji dolaze sa joystick-a
//prva verzija koda
Nakon kontrolisanja jednog H mosta bilo je potrebno napisati kod za kontrolu dva
//slika druge verzije koda
Poslednji izazov u kodu bilo je programiranje skretanja samog vozila
Pošto auto ima pogon od dva motora, skretanje bi se vršilo tako sto jedan uspori a drugi ubrza, gded bi se auto okretao oko sporijeg točka
//slika finalne verzije koda
Takođe je dodana opcija Switch, u slučaju da vozilo uradi nesto nepredvidivo

## IDEJE i ZAKLJUČCI

Ubgrade ovog projekta je definitivno bežična kontrola
Vozilu bi takođe pomogla lakša šasija kao i regulisaniji izvor napajanja
Da smo se bolje informisali o odnosu različitih komponenata verujem da bi smo imali više vremena da odradimo kako treba, bolje bi smo zalemili šeme i pre bi smo dizajnirali delove auta, takođe bi imali dovoljno vremena da više istražimo o wifi modulima i njima upravljamo vožnju auta.
Tokom ovog projekta smo naučili o FET tranzistorima, 3D modelovanju, i programiranju.
Ideja je da napravimo manji laksi i bolje zalemljen arduino auto koji bi smo koltrolisali pomoću wifi modula.
