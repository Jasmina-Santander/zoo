# zoo
Actividad Python
Imagina un juego donde puedes crear un zoológico y comenzar a criar diferentes tipos de animales. Digamos que por cada zoológico que crees puede haber varios animales diferentes. Comience creando una clase Animal y luego al menos 3 clases específicas de animales que hereden de Animal. (Tal vez leones, tigres y osos, ¡Dios mío!) Cada animal debe tener al menos un nombre, una edad, un nivel de salud y un nivel de felicidad. La clase Animal debe tener un método display_info que muestre el nombre, la salud y la felicidad del animal. También debe tener un método de alimentación que aumente la salud y la felicidad en 10.

En al menos una de las clases de Animal child que ha creado, agregue al menos un atributo único. Dele a cada animal diferentes niveles predeterminados de salud y felicidad. Los animales también deben responder al método de alimentación con diferentes niveles de cambios en la salud y la felicidad.

Una vez que haya probado sus diferentes animales y se sienta más cómodo con la herencia, cree una clase de zoológico para ayudar a manejar a todos sus animales.

Una forma de armar este zoológico es haciendo lo siguiente:

class Zoo:
    def __init__(self, zoo_name):
        self.animals = []
        self.name = zoo_name
    def add_lion(self, name):
        self.animals.append( Lion(name) )
    def add_tiger(self, name):
        self.animals.append( Tiger(name) )
    def print_all_info(self):
        print("-"*30, self.name, "-"*30)
        for animal in self.animals:
            animal.display_info()
zoo1 = Zoo("John's Zoo")
zoo1.add_lion("Nala")
zoo1.add_lion("Simba")
zoo1.add_tiger("Rajah")
zoo1.add_tiger("Shere Khan")
zoo1.print_all_info()
