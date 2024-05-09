# CÓDIGO BASE DE DATOS NOSQL

## Hernan Daniel Heenandez
## Albert Stive Ospina

Usar base de datos
```
use eventodeportivo;
```

Crear Colecciones 

### Deportistas
```
db.createCollection("deportistas")
```
### Equipos
```
db.createCollection("equipos")
```
### Entrenadores
```
db.createCollection("entrenadores")
```
### Arbitros
```
db.createCollection("arbitros")
```
### Encuentros Deportivos
```
db.createCollection("encuentrosDeportivos")
```
### tabla Posiciones
```
db.createCollection("tablaPosiciones")
```
### Resultados
```
db.createCollection("resultados")
```

# Inserción de Datos
### Deportitas

db.deportistas.insertMany([
    {
        nombres:"Daniel Felipe",
        apellidos:"Cortez Mendoza",
        documento:"12345",
        edad:"18",
        altura:1.80,
        peso: 72,
        rol:"Capitan"
    },
    {
        nombres:"Stiven",
        apellidos:"Ospina Avendaño",
        documento:"6789",
        edad:"19",
        altura:1.70,
        peso: 65,
        rol:"Rematador"
    },
    {
        nombres:"Andres Santiago",
        apellidos:"Gomez Pinzon",
        documento:"6780",
        edad:"18",
        altura:1.72,
        peso: 70,
        rol:"Libero"
    },
    {
        nombres:"Edwin",
        apellidos:"Corso Rojas",
        documento:"123",
        edad:"22",
        altura:1.72,
        peso: 70,
        rol:"Capitan"
    },
    {
        nombres:"Mateo",
        apellidos:"Castro Molina",
        documento:"45",
        edad:"20",
        altura:1.78,
        peso: 75,
        rol:"Colocador"
    },
    {
        nombres:"Gonzalo",
        apellidos:"Cabrera Martinez",
        documento:"67",
        edad:"19",
        altura:1.77,
        peso: 73,
        rol:"Remate"
    }
])

### Entrenadores

db.entrenadores.insertMany([
    {
        nombres:"Leonardo",
        apellidos:"Castro Rojas",
        documento:"8097",
        edad:"20",
        experiencia:"5 años"
    },
    {
        nombres:"Emilio",
        apellidos:"Rodriguez Lopez",
        documento:"4576",
        edad:"19",
        experiencia:"10 años"
    },
    {
        nombres:"Wilman",
        apellidos:"Calderon Torres",
        documento:"0896",
        edad:"20",
        experiencia:"7 años"
    },
    {
        nombres:"Javier",
        apellidos:"Jimenez Merchan",
        documento:"2531",
        edad:"19",
        experiencia:"15 años"
    },
    {
        nombres:"Mateo",
        apellidos:"Castro Molina",
        documento:"24857",
        edad:"20",
        experiencia:"9 años"
    },
    {
        nombres:"Gonzalo",
        apellidos:"Cabrera Martinez",
        documento:"6788",
        edad:"19",
        experiencia:"12 años"
    }
])

### Equipos
db.equipos.insertMany([
    {
        nombre:"Las aguilas",
        region: "Bogotá D.C",
        pais:"Colombia",
        participantes:["6789","123"],
        entrenador:"6788"
    },
    {
        nombre:"VoleyKins",
        region: "Medellin",
        pais:"Colombia",
        participantes:["45","67"],
        entrenador:"0896"
    },
    {
        nombre:"StartsDeports",
        region: "Bogotá D.C",
        pais:"Colombia",
        participantes:["6780"],
        entrenador:"4576"
    },
    {
        nombre:"NovaSports",
        region: "Bogotá D.C",
        pais:"Colombia",
        participantes:[],
        entrenador:"2531"
    },
    {
        nombre:"Geiguers",
        region: "Bogotá D.C",
        pais:"Colombia",
        participantes:[],
        entrenador:"24857"
    },
]) 
### Arbitros
db.arbitros.insertMany([
    {
        nombres:"Carlos",
        apellidos:"Gonzalez Beltran",
        documento:"6953",
        region:"20",
        experiencia:"5 años",
        disponibilidad:true
    },
    {
        nombres:"Carmen Alicia",
        apellidos:"Rojas Gomez",
        documento:"6953",
        region:"20",
        experiencia:"5 años",
        disponibilidad:false
    },
    {
        nombres:"Jennifer Andrea",
        apellidos:"Perez Bolivar",
        documento:"6953",
        region:"20",
        experiencia:"5 años",
        disponibilidad:true
    }
])
### Encuentros
db.encuentrosDeportivos.insertMany([
    {
        lugar:"Bogotá, instalación victory fitnes",
        fechaHora: "10-06-2024 14:00",
        duracion:"",
        equipos:["Las aguilas","StartsDeports"],
        arbitro:"6953"
    }
])
### Resultados
db.resultados.insertMany([
    {
        ganador:"Las aguilas",
        perdedor:"StartsDeports",
        sets:[
            {
                numeroset:"1",
                equipo:{
                    nombre:"Las aguilas",
                    puntos: "25"
                },
                rival:{
                    "nombre":"StartsDeports",
                    puntos: "17"
                }
            },
            {
                numeroset:"2",
                equipo:{
                    nombre:"Las aguilas",
                    puntos: "20"
                },
                rival:{
                    "nombre":"StartsDeports",
                    puntos: "25"
                }
            },
            {
                numeroset:"3",
                equipo:{
                    nombre:"Las aguilas",
                    puntos: "25"
                },
                rival:{
                    "nombre":"StartsDeports",
                    puntos: "21"
                }
            },
        ]
    }
])

### Tabla posiciones
db.tablaPosiciones.insertMany([
    {
        posicion:1,
        equipo:"Las aguilas",
        pj:1,
        pg:1,
        pp:0
    },
    {
        posicion:2,
        equipo:"StartsDeports",
        pj:1,
        pg:0,
        pp:1
    }
])
