# Módulo Hospital - Odoo 18

Este módulo permite gestionar pacientes, médicos y atenciones en un hospital.

## Preparar entorno (archivos y estructura)
<img width="605" height="556" alt="image" src="https://github.com/user-attachments/assets/3e6dd8f1-71dd-4851-8a4d-4bd6b9e4eb53" />

## Manifest.py:
<img width="903" height="500" alt="image" src="https://github.com/user-attachments/assets/6533af62-4b48-4557-81f6-d345f885d5ad" />


 ## hospital-views.xml:
<odoo>
    <record id="view_paciente_tree" model="ir.ui.view">
        <field name="name">hospital.paciente.tree</field>
        <field name="model">hospital.paciente</field>
        <field name="arch" type="xml">
            <list>
                <field name="name"/>
                <field name="sintomas"/>
            </list>
        </field>
    </record>

    <record id="view_paciente_form" model="ir.ui.view">
        <field name="name">hospital.paciente.form</field>
        <field name="model">hospital.paciente</field>
        <field name="arch" type="xml">
            <form>
                <sheet>
                    <group>
                        <field name="name"/>
                        <field name="sintomas"/>
                    </group>
                    <notebook>
                        <page string="Historial de Diagnósticos">
                            <field name="diagnostico_ids">
                                <list>
                                    <field name="fecha"/>
                                    <field name="medico_id"/>
                                    <field name="diagnostico"/>
                                </list>
                            </field>
                        </page>
                    </notebook>
                </sheet>
            </form>
        </field>
    </record>

    <record id="action_pacientes" model="ir.actions.act_window">
        <field name="name">Pacientes</field>
        <field name="res_model">hospital.paciente</field>
        <field name="view_mode">list,form</field>
    </record>

    <record id="action_medicos" model="ir.actions.act_window">
        <field name="name">Médicos</field>
        <field name="res_model">hospital.medico</field>
        <field name="view_mode">list,form</field>
    </record>

    <record id="action_diagnosticos" model="ir.actions.act_window">
        <field name="name">Diagnósticos</field>
        <field name="res_model">hospital.diagnostico</field>
        <field name="view_mode">list,form</field>
    </record>

    <menuitem id="menu_hospital_root" name="Hospital" sequence="10"/>
    <menuitem id="menu_pacientes" name="Pacientes" parent="menu_hospital_root" action="action_pacientes"/>
    <menuitem id="menu_medicos" name="Médicos" parent="menu_hospital_root" action="action_medicos"/>
    <menuitem id="menu_diagnosticos" name="Diagnósticos" parent="menu_hospital_root" action="action_diagnosticos"/>
</odoo>

 ## Models.py: 

<img width="901" height="802" alt="image" src="https://github.com/user-attachments/assets/114a834f-bafb-4f9f-a046-b103881e7225" />


### El .yml es e mismo q otras practicas.

### Ahora vamos a la BD y activamos el modulos buscando Gestion de Hospital:
<img width="1061" height="656" alt="image" src="https://github.com/user-attachments/assets/40ae9a5c-2d88-445d-8bf0-0789ac5afd49" />

<img width="1918" height="426" alt="image" src="https://github.com/user-attachments/assets/9b526390-2411-4d4f-a87b-3774577d58d4" />

<img width="1915" height="493" alt="image" src="https://github.com/user-attachments/assets/6291342e-7012-45e2-93a0-7a1ecf9d5ecb" />












http://localhost:8069/odoo/apps

