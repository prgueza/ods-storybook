# Accordion

Use Accordion para almacenar contenidos.

## Uso básico

Puede expandir varios paneles


```
<ods-accordion v-model="activeNames" @change="handleChange">
  <ods-accordion-item title="Consistency" name="1">
    <div>Consistent with real life: in line with the process and logic of real life, and comply with languages and habits that the users are used to;</div>
    <div>Consistent within interface: all elements should be consistent, such as: design style, icons and texts, position of elements, etc.</div>
  </ods-accordion-item>
  <ods-accordion-item title="Feedback" name="2">
    <div>Operation feedback: enable the users to clearly perceive their operations by style updates and interactive effects;</div>
    <div>Visual feedback: reflect current state by updating or rearranging elements of the page.</div>
  </ods-accordion-item>
  <ods-accordion-item title="Efficiency" name="3">
    <div>Simplify the process: keep operating process simple and intuitive;</div>
    <div>Definite and clear: enunciate your intentions clearly so that the users can quickly understand and make decisions;</div>
    <div>Easy to identify: the interface should be straightforward, which helps the users to identify and frees them from memorizing and recalling.</div>
  </ods-accordion-item>
  <ods-accordion-item title="Controllability" name="4">
    <div>Decision making: giving advices about operations is acceptable, but do not make decisions for the users;</div>
    <div>Controlled consequences: users should be granted the freedom to operate, including canceling, aborting or terminating current operation.</div>
  </ods-accordion-item>
</ods-accordion>
<script>
  {
    data() {
      return {
        activeNames: ['1']
      };
    },
    methods: {
      handleChange(val) {
        console.log(val);
      }
    }
  }
</script>
```


## Acordeón

En modo acordeón sólo un panel puede ser expandido a la vez

Activa el modo acordeón usado el atributo `accordion`.

```
<ods-accordion v-model="activeName" accordion>
  <ods-accordion-item title="Consistency" name="1">
    <div>Consistent with real life: in line with the process and logic of real life, and comply with languages and habits that the users are used to;</div>
    <div>Consistent within interface: all elements should be consistent, such as: design style, icons and texts, position of elements, etc.</div>
  </ods-accordion-item>
  <ods-accordion-item title="Feedback" name="2">
    <div>Operation feedback: enable the users to clearly perceive their operations by style updates and interactive effects;</div>
    <div>Visual feedback: reflect current state by updating or rearranging elements of the page.</div>
  </ods-accordion-item>
  <ods-accordion-item title="Efficiency" name="3">
    <div>Simplify the process: keep operating process simple and intuitive;</div>
    <div>Definite and clear: enunciate your intentions clearly so that the users can quickly understand and make decisions;</div>
    <div>Easy to identify: the interface should be straightforward, which helps the users to identify and frees them from memorizing and recalling.</div>
  </ods-accordion-item>
  <ods-accordion-item title="Controllability" name="4">
    <div>Decision making: giving advices about operations is acceptable, but do not make decisions for the users;</div>
    <div>Controlled consequences: users should be granted the freedom to operate, including canceling, aborting or terminating current operation.</div>
  </ods-accordion-item>
</ods-accordion>
<script>
  {
    data() {
      return {
        activeName: '1'
      };
    }
  }
</script>
```


## Título personalizado

Además de usar el atributo `title`, se puede personalizar el título del panel con slots con nombre, esto hace posible agregar contenido personalizado, por ejemplo: iconos.


```
<ods-accordion accordion>
  <ods-accordion-item name="1">
    <template slot="title">
      Consistency <ods-icon name="info" size="16"></ods-icon>
    </template>
    <div>Consistent with real life: in line with the process and logic of real life, and comply with languages and habits that the users are used to;</div>
    <div>Consistent within interface: all elements should be consistent, such as: design style, icons and texts, position of elements, etc.</div>
  </ods-accordion-item>
  <ods-accordion-item title="Feedback" name="2">
    <div>Operation feedback: enable the users to clearly perceive their operations by style updates and interactive effects;</div>
    <div>Visual feedback: reflect current state by updating or rearranging elements of the page.</div>
  </ods-accordion-item>
  <ods-accordion-item title="Efficiency" name="3">
    <div>Simplify the process: keep operating process simple and intuitive;</div>
    <div>Definite and clear: enunciate your intentions clearly so that the users can quickly understand and make decisions;</div>
    <div>Easy to identify: the interface should be straightforward, which helps the users to identify and frees them from memorizing and recalling.</div>
  </ods-accordion-item>
  <ods-accordion-item title="Controllability" name="4">
    <div>Decision making: giving advices about operations is acceptable, but do not make decisions for the users;</div>
    <div>Controlled consequences: users should be granted the freedom to operate, including canceling, aborting or terminating current operation.</div>
  </ods-accordion-item>
</ods-accordion>
```


## Atributos de Accordion
| Atributo  | Descripción                           | Tipo                                     | Valores aceptados | Por defecto |
| --------- | ------------------------------------- | ---------------------------------------- | ----------------- | ----------- |
| accordion | especifica si activa el modo acordeón | boolean                                  | —                 | false       |
| value     | panel activo                          | string (modo acordeón)/array (No modo acordeón) | —                 | —           |

## Eventos de Accordion
| Nombre de Evento | Descripción                              | Parametros                               |
| ---------------- | ---------------------------------------- | ---------------------------------------- |
| change           | se dispara cuando los paneles activos cambian | activeNames: array (No modo acordeón)/string (modo acordeón) |


## Atributos de Accordion Item
| Atributo | Descripción                   | Tipo          | Valores aceptados | Por defecto |
| -------- | ----------------------------- | ------------- | ----------------- | ----------- |
| name     | identificador único del panel | string/number | —                 | —           |
| title    | título del panel              | string        | —                 | —           |