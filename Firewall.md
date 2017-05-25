# TALLAFOCS
## 1.Tallafocs
#### 1.Què es un sistema tallafocs? Quina és la seva finalitat?
És un element de maquinaria o programari utilitzat en una xarxa d'equips informàtics per controlar les comunicacions.
#### 2.Quines generacions de tallafocs hi ha hagut i què millorava cadascun?
El primer document publicat para la tecnología firewall va ser en 1988, quan l'equip d'enginyers Digital Equipment Corporation (DEC) desenvolupada amb els sistemes de filtrat conegut com a tallafocs. La segona versió incorporava una ordenació de les IP's. La tercera era un mètode que actuava sota la capa d'aplicaciṕo del mètode OSI.
#### 3. Quines capes té el model OSI?
El model de interconnexió de sistemes oberts, més conegut com a Model OSI, es un model de referència per a protocols de red.

![image](http://2.bp.blogspot.com/-JojgFWojay4/ThiIcdP7MOI/AAAAAAAAAEA/vxl_J757Wr0/s1600/modelo+Osi.jpg)

#### 4. Quines capes té el model TCP/IP? En aquest cas feu una breu descripció de les funcionalitats de cada capa.
El model TCP/IP es una descripció de protocols de xarxa que va ser desenvolupat en 1970. Aquest model es utiliztat per a comunicacions en xarxes TCP/IP

![image](https://libroccna.files.wordpress.com/2013/01/modelo-de-protocolo-tcp_ip.png)

#### 5. A quina capa/capes sol treballar tradicionalment un tallafocs?
Treballa en dues capes; la capa de xarxa (com filtrat de paquets IP) i la capa d'aplicació

## 2.Tallafocs Linux

#### 1.Busqueu quins són els tradicionals sistemes de tallafocs incorporats en linux i anomeneu-los
- CSF(ConfigServer & Security Firewall)
- ShoreWall
- APF(Advanced Policy Firewall)
- iptables
- firewalld
#### 2.Quins dels anteriors tallafocs estan instal.lats al fedora de classe? Com ho comproveu?
- Iptables
- Firewalld
Son els que formen part de Linux avui en dia.
#### 3. Algun dels anteriors tallafocs es troba activat?
L'únic que és troba activat es firewalld
#### 4. Instal.leu el servidor web httpd o nginx i activeu-ne el servei (dnf installl ...  ; systemctl ....). Indiqueu les comandes i comproveu que des d'una altra màquina podeu accedir via web a la vostra IP (digueu-li a un company). Hauria de sortir la plana per defecte.
- #dnf isntall -y nginx
- #systemctl start nginx
![image](https://fotos.subefotos.com/7e15d87ab3f2d3dd940072951e5c4603o.png)
