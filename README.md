class Jugador1:
    pass
    jugador1="Batman"
    Vida="100%"

class Jugador2:
    pass
    jugador2="Iron Man"
    vida2="100%"
    
    
from Jugador1 import Jugador1
from Jugador2 import Jugador2

class Juego(Jugador1,Jugador2):
    pass 
    def __init__(self,restarVida,TotalVida):
        self.restarVida=restarVida
        self.TotalVida=TotalVida
        
    def InicioPartida(self):
        return"\x1b[1;36m"+"//Inicia el juego//\n{} le da un golpe a {} le quita {} de vida \n el personaje queda con un total  de vida de //{}//".format(Jugador1.jugador1,Jugador2.jugador2,self.restarVida,self.TotalVida)
        

Partida = Juego("30%","70%")
print(Partida.InicioPartida())
