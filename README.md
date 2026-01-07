# Módulo Hospital - Odoo 18

Este módulo permite gestionar pacientes, médicos y atenciones en un hospital.

## Preparar entorno
Creamos todo el entorno de carpetas necesarias como el .yml, los archivos paciente.py, medico.py...etc, los addoons, conf, todos los .xml, etc:

<img width="568" height="520" alt="image" src="https://github.com/user-attachments/assets/aae5d386-eb7a-4662-bac9-c112cecfb585" />


## Crear la base de datos
Entramos en `http://localhost:8069` y crear nueva base de datos.
<img width="1268" height="920" alt="image" src="https://github.com/user-attachments/assets/19d21172-f9a3-40fb-b5df-749bb59c1b63" />

## Crear módulo Hospital

- Carpeta: `addons/hospital`.
- Archivos base: `__manifest__.py`, `__init__.py`.
- Subcarpeta `models` con `__init__.py`.
- Crear modelos: `paciente.py`, `medico.py`, `atencion.py`.


## Crear vistas
- Crear XML en `views/` para pacientes, médicos y atenciones.
- Definir formularios y listas.
- Enlazar con el módulo desde `__manifest__.py`.


## Instalar módulo desde Odoo


## 8. Probar funcionalidad

.










http://localhost:8069/odoo/apps

