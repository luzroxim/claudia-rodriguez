hide: 
- toc
# ✂️ Corte láser

- **Created:** Junio 2026
- **Tags:** Experimentación, Materiales, Corte láser, diseño textil

![Corte láser](../images/proyecto/9.jpg)

## Descripción

Esta ficha describe las pruebas de corte láser realizadas en la fase de experimentación. El corte láser es una técnica versátil que permite trabajar con diversos materiales y obtener resultados precisos.

## El archivo

Para realizar un corte láser necesitamos trabajar con archivos vectoriales 2D, usamos softwares como Illustrator o Inkscape para generar estos archivos. 

Nuestro dibujo vectorial funciona como un archivo CAD que contiene los datos de nuestro diseño. Para poder trabajar con una cortadora láser, debemos usar un software que transforme esa información en una trayectoria (software CAD), indicándole a la máquina cómo desplazarse dentro de los ejes XY para trazar nuestro dibujo de la manera más eficiente.

Por lo general, cada cortadora láser tendrá su propio software. En el Lab de Minas usamos RDworks.

En este programa podemos setear distintos parámetros dependiendo de los materiales que deseemos cortar y la potencia de la máquina. (esto lo veremos en cada situación)

Paso a paso básico para el uso de una cortadora láser.

<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Flujo de trabajo — Cortadora láser</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: sans-serif; background: #f5f4f0; color: #1a1a18; padding: 32px 24px; max-width: 680px; margin: 0 auto; }
  h1 { font-size: 18px; font-weight: 500; margin-bottom: 6px; }
  .subtitle { font-size: 13px; color: #6b6a64; margin-bottom: 24px; }
  .section-label { font-size: 11px; font-weight: 500; letter-spacing: 0.06em; text-transform: uppercase; color: #9c9a92; margin: 20px 0 8px 4px; }
  .step-card { display: flex; align-items: flex-start; gap: 14px; background: #fff; border: 0.5px solid #d3d1c7; border-radius: 12px; padding: 14px 16px; margin-bottom: 10px; }
  .step-num { min-width: 32px; height: 32px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: 500; font-size: 14px; flex-shrink: 0; }
  .num-blue { background: #e6f1fb; color: #185fa5; }
  .num-green { background: #eaf3de; color: #3b6d11; }
  .step-body { flex: 1; }
  .step-title { font-size: 14px; font-weight: 500; color: #1a1a18; margin-bottom: 4px; display: flex; align-items: center; gap: 8px; }
  .step-emoji { font-size: 16px; }
  .step-desc { font-size: 13px; color: #5f5e5a; line-height: 1.55; }
  .step-detail { font-size: 12px; color: #888780; background: #f5f4f0; border: 0.5px solid #d3d1c7; border-radius: 8px; padding: 8px 10px; margin-top: 8px; font-family: monospace; line-height: 1.7; }
  .connector { width: 2px; height: 12px; background: #d3d1c7; margin: 0 0 0 22px; }
  .warning-box { background: #faeeda; border: 0.5px solid #f0c060; border-radius: 12px; padding: 14px 16px; margin-top: 20px; }
  .warning-title { font-size: 14px; font-weight: 500; color: #854f0b; margin-bottom: 10px; display: flex; align-items: center; gap: 8px; }
  .warning-item { display: flex; align-items: flex-start; gap: 8px; font-size: 13px; color: #5f5e5a; margin-bottom: 7px; line-height: 1.5; }
  .warning-item:last-child { margin-bottom: 0; }
  .dot { width: 6px; height: 6px; border-radius: 50%; background: #ba7517; flex-shrink: 0; margin-top: 7px; }
  strong { font-weight: 500; }
</style>
</head>
<body>

<h1>Flujo de trabajo — Cortadora láser</h1>
<p class="subtitle">Paso a paso desde el encendido hasta el corte</p>

<p class="section-label">Preparación</p>

<div class="step-card">
  <div class="step-num num-green">1</div>
  <div class="step-body">
    <p class="step-title"><span class="step-emoji">🔌</span> Encendido y ventilación</p>
    <p class="step-desc">Encender la máquina y verificar que el extractor de aire esté funcionando.</p>
  </div>
</div>
<div class="connector"></div>

<div class="step-card">
  <div class="step-num num-blue">2</div>
  <div class="step-body">
    <p class="step-title"><span class="step-emoji">💾</span> Cargar archivo desde USB</p>
    <p class="step-desc">Copiar el archivo desde la memoria USB a la máquina usando la interfaz:</p>
    <div class="step-detail">
      File → (mover a la derecha hasta el final de la fila)<br>
      Undisk+ → Enter → Read U file → Enter<br>
      Copy to mem → Enter → Escape<br><br>
      Luego: File → (buscar el archivo recién copiado) → Enter
    </div>
  </div>
</div>
<div class="connector"></div>

<p class="section-label">Configuración</p>

<div class="step-card">
  <div class="step-num num-blue">3</div>
  <div class="step-body">
    <p class="step-title"><span class="step-emoji">🖥️</span> Verificar parámetros</p>
    <p class="step-desc">El display muestra una vista previa del archivo con velocidad, potencia y capas de corte vs. grabado identificadas por color.</p>
  </div>
</div>
<div class="connector"></div>

<div class="step-card">
  <div class="step-num num-blue">4</div>
  <div class="step-body">
    <p class="step-title"><span class="step-emoji">🎯</span> Definir origen</p>
    <p class="step-desc">Usar las flechas <strong>X/Y</strong> para posicionar el puntero láser en el origen deseado. Confirmar con el botón <strong>Origin</strong>.</p>
  </div>
</div>
<div class="connector"></div>

<div class="step-card">
  <div class="step-num num-blue">5</div>
  <div class="step-body">
    <p class="step-title"><span class="step-emoji">📏</span> Cargar material y ajustar foco</p>
    <p class="step-desc">Verificar la distancia entre el puntero láser y el material. Lo estándar es <strong>7 mm</strong>, pero puede variar según el material y la máquina.</p>
  </div>
</div>
<div class="connector"></div>

<p class="section-label">Verificación final</p>

<div class="step-card">
  <div class="step-num num-green">6</div>
  <div class="step-body">
    <p class="step-title"><span class="step-emoji">⬜</span> Frame — recorrido en seco</p>
    <p class="step-desc">Presionar <strong>Frame</strong>: la boquilla recorre el área de trabajo sin cortar. Verificar que el material esté bien ubicado antes de continuar.</p>
  </div>
</div>
<div class="connector"></div>

<div class="step-card">
  <div class="step-num num-green">7</div>
  <div class="step-body">
    <p class="step-title"><span class="step-emoji">▶️</span> ¡Iniciar corte!</p>
    <p class="step-desc">Presionar <strong>Start</strong> para comenzar el trabajo.</p>
  </div>
</div>

<div class="warning-box">
  <p class="warning-title">⚠️ Seguridad — siempre presentes</p>
  <div class="warning-item"><div class="dot"></div><span>Trabajar siempre con la cámara cerrada y protección ocular.</span></div>
  <div class="warning-item"><div class="dot"></div><span>No dejar la máquina sola — estar cerca ante cualquier falla.</span></div>
  <div class="warning-item"><div class="dot"></div><span>Válvula de seguridad a mano: presionarla detiene el trabajo de inmediato.</span></div>
  <div class="warning-item"><div class="dot"></div><span>Si hay chispas o llama, <strong>nunca usar agua</strong> — usar algo que quite el oxígeno.</span></div>
</div>

</body>
</html>

### Ficha 1


## Plantillas para plisado

📄[[Plantillas disponibles](https://drive.google.com/drive/folders/1gPYXmxWb4KO5qtIqeHYtKbnYUo5L9nUC?usp=drive_link)] 

