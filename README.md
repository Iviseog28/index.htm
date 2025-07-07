<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Taller Mecánico Ensigna</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&family=Open+Sans&display=swap');

  * { box-sizing: border-box; }

  body {
    margin: 0; padding: 0;
    font-family: 'Open Sans', sans-serif;
    background-color: #e8f0f7;
    color: #222;
  }

  header {
    background-color: #003366;
    color: white;
    padding: 10px 0;
    position: relative;
    overflow: hidden;
  }

  .titulo-animado {
    white-space: nowrap;
    display: flex;
    align-items: center;
    padding-left: 100%;
    animation: moverTitulo 15s linear infinite;
    font-family: 'Montserrat', sans-serif;
    font-size: 2.5rem;
    font-weight: 700;
    user-select: none;
    gap: 20px;
  }

  .titulo-animado img {
    height: 50px;
    width: auto;
  }

  @keyframes moverTitulo {
    0% { transform: translateX(0); }
    100% { transform: translateX(-100%); }
  }

  nav {
    background-color: #00509e;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    padding: 10px 0;
  }

  nav a {
    color: white;
    text-decoration: none;
    margin: 0 15px;
    font-weight: 600;
    font-size: 1.1rem;
    padding: 8px 12px;
    border-radius: 6px;
    transition: background-color 0.3s;
  }

  nav a:hover, nav a.active {
    background-color: #014f86;
  }

  main {
    max-width: 900px;
    margin: 20px auto;
    background: white;
    border-radius: 12px;
    box-shadow: 0 0 15px rgba(0,0,0,0.1);
    padding: 20px 30px;
  }

  section {
    display: none;
  }

  section.active {
    display: block;
  }

  h2 {
    font-family: 'Montserrat', sans-serif;
    color: #003366;
    margin-top: 0;
  }

  p, ul {
    line-height: 1.5;
  }

  ul {
    padding-left: 20px;
  }

  img.taller {
    display: block;
    max-width: 100%;
    margin: 10px auto 20px auto;
    border-radius: 10px;
    box-shadow: 0 0 8px rgba(0,0,0,0.15);
  }

  form label {
    display: block;
    margin-top: 15px;
    font-weight: 600;
  }

  input, select, textarea {
    width: 100%;
    padding: 8px;
    margin-top: 6px;
    border: 1px solid #ccc;
    border-radius: 6px;
    font-size: 1rem;
    font-family: inherit;
  }

  textarea {
    resize: vertical;
    min-height: 60px;
  }

  button {
    margin-top: 20px;
    background-color: #00509e;
    border: none;
    color: white;
    padding: 12px 25px;
    font-size: 1.1rem;
    border-radius: 8px;
    cursor: pointer;
    font-weight: 700;
    transition: background-color 0.3s;
  }

  button:hover {
    background-color: #003b66;
  }

  .mensaje {
    margin-top: 15px;
    font-weight: 600;
    color: green;
  }

  .mensaje.error {
    color: red;
  }

  table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 15px;
  }

  th, td {
    border: 1px solid #ccc;
    padding: 8px 12px;
    text-align: left;
  }

  footer {
    text-align: center;
    margin: 30px 0 10px 0;
    color: #555;
    font-size: 0.9rem;
  }

  @media (max-width: 600px) {
    nav { flex-direction: column; }
    nav a { margin: 8px 0; }
    .titulo-animado {
      font-size: 1.8rem;
      gap: 12px;
    }
    .titulo-animado img { height: 40px; }
  }
</style>
</head>
<body>

<header>
  <div class="titulo-animado">
    <img src="https://marketplace.canva.com/EAFCyC9aHzU/1/0/1600w/canva-logo-para-taller-mec%C3%A1nico-ilustrado-cjEg8SslVIU.jpg" alt="Logo Ensigna" />
    Bienvenido al Taller Mecánico Ensigna - Servicio de calidad y confianza
    <img src="https://marketplace.canva.com/EAFCyC9aHzU/1/0/1600w/canva-logo-para-taller-mec%C3%A1nico-ilustrado-cjEg8SslVIU.jpg" alt="Logo Ensigna" />
  </div>
</header>

<nav>
  <a href="#" class="active" data-seccion="inicio">Inicio</a>
  <a href="#" data-seccion="info">Información del Taller</a>
  <a href="#" data-seccion="registro">Registrar Cliente y Vehículo</a>
  <a href="#" data-seccion="asignar">Asignar Mecánico</a>
  <a href="#" data-seccion="repuestos">Agregar Repuestos</a>
  <a href="#" data-seccion="factura">Ver Factura</a>
  <a href="#" data-seccion="consulta">Consultar Estado</a>
</nav>

<main>
  <!-- Inicio / bienvenida -->
  <section id="inicio" class="active">
    <h2>Bienvenido a Ensigna</h2>
    <img src="https://marketplace.canva.com/EAFCyC9aHzU/1/0/1600w/canva-logo-para-taller-mec%C3%A1nico-ilustrado-cjEg8SslVIU.jpg" alt="Logo Taller Ensigna" class="taller" />
    <p>En Ensigna ofrecemos servicios integrales de reparación y mantenimiento para tu vehículo con la más alta calidad y confianza.</p>
    <p>Nuestro equipo de mecánicos altamente capacitados se dedica a diagnosticar y resolver cualquier problema mecánico, utilizando repuestos originales y técnicas modernas.</p>
    <p>Contamos con un sistema organizado para garantizar transparencia en los costos, tiempos de entrega y atención personalizada a cada cliente.</p>
  </section>

  <!-- Información del taller -->
  <section id="info">
    <h2>Información del Taller</h2>
    <p><strong>Misión:</strong> Brindar servicios mecánicos especializados con compromiso y profesionalismo, asegurando la satisfacción y seguridad de nuestros clientes.</p>
    <p><strong>Visión:</strong> Ser el taller mecánico líder en la región, reconocido por la calidad de nuestro trabajo y la confianza que depositan en nosotros.</p>
    <p><strong>Valores:</strong></p>
    <ul>
      <li>Compromiso con el cliente</li>
      <li>Responsabilidad</li>
      <li>Trabajo en equipo</li>
      <li>Honestidad y transparencia</li>
      <li>Innovación y mejora continua</li>
    </ul>
    <img src="https://cdn.pixabay.com/photo/2018/03/06/18/52/wrench-3207852_1280.jpg" alt="Herramientas de taller" class="taller" />
  </section>

  <!-- Registro cliente y vehículo -->
  <section id="registro">
    <h2>Registrar Cliente y Vehículo</h2>
    <form id="formRegistro">
      <label for="dniCliente">DNI *</label>
      <input type="text" id="dniCliente" required>
      <label for="nombreCliente">Nombre *</label>
      <input type="text" id="nombreCliente" required>
      <label for="apellidosCliente">Apellidos</label>
      <input type="text" id="apellidosCliente">
      <label for="direccionCliente">Dirección</label>
      <input type="text" id="direccionCliente">
      <label for="telefonoCliente">Teléfono</label>
      <input type="text" id="telefonoCliente">

      <label for="matriculaVehiculo">Matrícula *</label>
      <input type="text" id="matriculaVehiculo" required>
      <label for="modeloVehiculo">Modelo</label>
      <input type="text" id="modeloVehiculo">
      <label for="colorVehiculo">Color</label>
      <input type="text" id="colorVehiculo">
      <label for="fechaEntrada">Fecha de entrada *</label>
      <input type="date" id="fechaEntrada" required>
      <label for="horaEntrada">Hora de entrada *</label>
      <input type="time" id="horaEntrada" required>

      <button type="submit">Registrar</button>
    </form>
    <div class="mensaje" id="mensajeRegistro"></div>
  </section>

  <!-- Asignar mecánico -->
  <section id="asignar">
    <h2>Asignar Mecánico</h2>
    <form id="formAsignarMecanico">
      <label for="selectVehiculos">Seleccione vehículo (Matrícula) *</label>
      <select id="selectVehiculos" required></select>

      <label for="selectMecanicos">Seleccione mecánico *</label>
      <select id="selectMecanicos" required></select>

      <button type="submit">Asignar</button>
    </form>
    <div class="mensaje" id="mensajeAsignacion"></div>
  </section>

  <!-- Agregar repuestos -->
  <section id="repuestos">
    <h2>Agregar Repuestos a Reparación</h2>
    <form id="formRepuestos">
      <label for="selectVehiculosRepuesto">Seleccione vehículo (Matrícula) *</label>
      <select id="selectVehiculosRepuesto" required></select>

      <label for="nombreRepuesto">Nombre del repuesto *</label>
      <input type="text" id="nombreRepuesto" required>
      <label for="cantidadRepuesto">Cantidad *</label>
      <input type="number" id="cantidadRepuesto" min="1" value="1" required>
      <label for="precioRepuesto">Precio unitario *</label>
      <input type="number" id="precioRepuesto" min="0" step="0.01" required>

      <button type="submit">Agregar repuesto</button>
    </form>
    <div class="mensaje" id="mensajeRepuesto"></div>

    <div id="listaRepuestos"></div>
  </section>

  <!-- Ver factura -->
  <section id="factura">
    <h2>Factura de Reparación</h2>
    <label for="selectVehiculosFactura">Seleccione vehículo (Matrícula)</label>
    <select id="selectVehiculosFactura"></select>
    <button onclick="mostrarFactura()">Mostrar Factura</button>
    <div id="facturaResultado"></div>
  </section>

  <!-- Consultar estado -->
  <section id="consulta">
    <h2>Consultar Estado de Reparación</h2>
    <label for="dniConsulta">Ingrese DNI del cliente</label>
    <input type="text" id="dniConsulta" />
    <button onclick="consultarEstado()">Consultar</button>
    <div id="resultadoConsulta"></div>
  </section>
</main>

<footer>
  &copy; 2025 Taller Mecánico Ensigna. IVIS ELIUTH ORTIX GÓMEZ N.L.29.
</footer>

<script>
  // Datos mecánicos iniciales
  const mecanicos = [
    {id: 1, nombre: "Juan", apellidos: "Pérez", estado: "Libre"},
    {id: 2, nombre: "María", apellidos: "López", estado: "Libre"},
    {id: 3, nombre: "Carlos", apellidos: "Gómez", estado: "Libre"}
  ];

  // Datos guardados en memoria
  const clientes = [];
  const vehiculos = [];
  const reparaciones = [];

  // Manejo de navegación y secciones
  const navLinks = document.querySelectorAll('nav a');
  navLinks.forEach(link => {
    link.addEventListener('click', e => {
      e.preventDefault();
      navLinks.forEach(l => l.classList.remove('active'));
      link.classList.add('active');
      mostrarSeccion(link.dataset.seccion);
    });
  });

  function mostrarSeccion(id) {
    document.querySelectorAll('main section').forEach(sec => sec.classList.remove('active'));
    const seccion = document.getElementById(id);
    if(seccion) seccion.classList.add('active');
    limpiarMensajes();

    if(['asignar','repuestos','factura'].includes(id)){
      actualizarSelectsVehiculos();
    }
    if(id === 'asignar'){
      actualizarSelectsMecanicos();
    }
  }

  function limpiarMensajes(){
    ['mensajeRegistro','mensajeAsignacion','mensajeRepuesto','facturaResultado','resultadoConsulta'].forEach(id => {
      const el = document.getElementById(id);
      if(el) el.innerHTML = '';
    });
    document.getElementById('listaRepuestos').innerHTML = '';
  }

  // Registro Cliente y Vehículo
  document.getElementById('formRegistro').addEventListener('submit', e => {
    e.preventDefault();

    const dni = document.getElementById('dniCliente').value.trim();
    const nombre = document.getElementById('nombreCliente').value.trim();
    const apellidos = document.getElementById('apellidosCliente').value.trim();
    const direccion = document.getElementById('direccionCliente').value.trim();
    const telefono = document.getElementById('telefonoCliente').value.trim();

    const matricula = document.getElementById('matriculaVehiculo').value.trim();
    const modelo = document.getElementById('modeloVehiculo').value.trim();
    const color = document.getElementById('colorVehiculo').value.trim();
    const fechaEntrada = document.getElementById('fechaEntrada').value;
    const horaEntrada = document.getElementById('horaEntrada').value;

    if(!dni || !nombre || !matricula || !fechaEntrada || !horaEntrada){
      mostrarMensaje('mensajeRegistro', "Por favor, complete todos los campos obligatorios.", true);
      return;
    }

    if(clientes.some(c => c.dni === dni) === false){
      clientes.push({dni,nombre,apellidos,direccion,telefono});
    }

    if(vehiculos.some(v => v.matricula === matricula)){
      mostrarMensaje('mensajeRegistro', "La matrícula ya está registrada.", true);
      return;
    }

    vehiculos.push({matricula,modelo,color,fechaEntrada,horaEntrada,clienteDni:dni});
    mostrarMensaje('mensajeRegistro', `Cliente y vehículo registrados correctamente.`);
    e.target.reset();
    actualizarSelectsVehiculos();
  });

  function mostrarMensaje(id, texto, esError=false){
    const el = document.getElementById(id);
    el.textContent = texto;
    el.className = esError ? 'mensaje error' : 'mensaje';
  }

  // Actualizar selects vehículos
  function actualizarSelectsVehiculos(){
    ['selectVehiculos','selectVehiculosRepuesto','selectVehiculosFactura'].forEach(id => {
      const sel = document.getElementById(id);
      if(!sel) return;
      sel.innerHTML = '';
      if(vehiculos.length === 0){
        sel.innerHTML = '<option value="">No hay vehículos registrados</option>';
        return;
      }
      vehiculos.forEach(v => {
        const opt = document.createElement('option');
        opt.value = v.matricula;
        opt.textContent = v.matricula + (v.modelo ? ' (' + v.modelo + ')' : '');
        sel.appendChild(opt);
      });
    });
  }

  // Actualizar selects mecánicos libres
  function actualizarSelectsMecanicos(){
    const sel = document.getElementById('selectMecanicos');
    sel.innerHTML = '';
    const libres = mecanicos.filter(m => m.estado === 'Libre');
    if(libres.length === 0){
      sel.innerHTML = '<option value="">No hay mecánicos libres</option>';
      return;
    }
    libres.forEach(m => {
      const opt = document.createElement('option');
      opt.value = m.id;
      opt.textContent = `${m.nombre} ${m.apellidos}`;
      sel.appendChild(opt);
    });
  }

  // Asignar mecánico
  document.getElementById('formAsignarMecanico').addEventListener('submit', e => {
    e.preventDefault();
    const vehiculoMatricula = document.getElementById('selectVehiculos').value;
    const mecanicoId = parseInt(document.getElementById('selectMecanicos').value);

    if(!vehiculoMatricula || !mecanicoId){
      mostrarMensaje('mensajeAsignacion', "Seleccione vehículo y mecánico.", true);
      return;
    }

    if(reparaciones.some(r => r.vehiculoMatricula === vehiculoMatricula)){
      mostrarMensaje('mensajeAsignacion', "Este vehículo ya tiene un mecánico asignado.", true);
      return;
    }

    reparaciones.push({vehiculoMatricula,mecanicoId,repuestos:[],precioManoObra:0,fechaEntrega:null,estado:'En reparación'});
    const mec = mecanicos.find(m => m.id === mecanicoId);
    mec.estado = 'Ocupado';

    mostrarMensaje('mensajeAsignacion', `Mecánico asignado al vehículo ${vehiculoMatricula}.`);
    actualizarSelectsMecanicos();
  });

  // Agregar repuestos
  document.getElementById('formRepuestos').addEventListener('submit', e => {
    e.preventDefault();

    const vehiculoMatricula = document.getElementById('selectVehiculosRepuesto').value;
    const nombre = document.getElementById('nombreRepuesto').value.trim();
    const cantidad = parseInt(document.getElementById('cantidadRepuesto').value);
    const precio = parseFloat(document.getElementById('precioRepuesto').value);

    if(!vehiculoMatricula || !nombre || cantidad <= 0 || precio < 0){
      mostrarMensaje('mensajeRepuesto', "Complete todos los campos correctamente.", true);
      return;
    }

    const reparacion = reparaciones.find(r => r.vehiculoMatricula === vehiculoMatricula);
    if(!reparacion){
      mostrarMensaje('mensajeRepuesto', "No hay mecánico asignado para este vehículo.", true);
      return;
    }

    reparacion.repuestos.push({nombre,cantidad,precio});
    mostrarMensaje('mensajeRepuesto', "Repuesto agregado.");
    e.target.reset();
    mostrarListaRepuestos(vehiculoMatricula);
  });

  function mostrarListaRepuestos(matricula){
    const div = document.getElementById('listaRepuestos');
    div.innerHTML = '';
    const reparacion = reparaciones.find(r => r.vehiculoMatricula === matricula);
    if(!reparacion || reparacion.repuestos.length === 0){
      div.innerHTML = '<p>No hay repuestos agregados para este vehículo.</p>';
      return;
    }
    let html = '<h3>Repuestos agregados:</h3><table><thead><tr><th>Nombre</th><th>Cantidad</th><th>Precio Unitario</th><th>Total</th></tr></thead><tbody>';
    reparacion.repuestos.forEach(r => {
      const total = (r.cantidad * r.precio).toFixed(2);
      html += `<tr><td>${r.nombre}</td><td>${r.cantidad}</td><td>$${r.precio.toFixed(2)}</td><td>$${total}</td></tr>`;
    });
    html += '</tbody></table>';
    div.innerHTML = html;
  }

  document.getElementById('selectVehiculosRepuesto').addEventListener('change', e => {
    mostrarListaRepuestos(e.target.value);
  });

  // Mostrar factura
  function mostrarFactura(){
    const sel = document.getElementById('selectVehiculosFactura');
    const matricula = sel.value;
    const div = document.getElementById('facturaResultado');
    div.innerHTML = '';

    if(!matricula){
      div.textContent = 'Seleccione un vehículo.';
      return;
    }

    const reparacion = reparaciones.find(r => r.vehiculoMatricula === matricula);
    if(!reparacion){
      div.textContent = 'No hay reparación registrada para este vehículo.';
      return;
    }

    let html = `<h3>Factura para vehículo: ${matricula}</h3>`;

    // Datos cliente
    const vehiculo = vehiculos.find(v => v.matricula === matricula);
    const cliente = clientes.find(c => c.dni === vehiculo.clienteDni);
    if(cliente){
      html += `<p><strong>Cliente:</strong> ${cliente.nombre} ${cliente.apellidos}</p>`;
      html += `<p><strong>DNI:</strong> ${cliente.dni}</p>`;
    }

    // Mecánico
    const mec = mecanicos.find(m => m.id === reparacion.mecanicoId);
    if(mec){
      html += `<p><strong>Mecánico:</strong> ${mec.nombre} ${mec.apellidos}</p>`;
    }

    // Repuestos
    if(reparacion.repuestos.length === 0){
      html += '<p>No se han agregado repuestos.</p>';
    } else {
      html += '<table><thead><tr><th>Repuesto</th><th>Cantidad</th><th>Precio Unitario</th><th>Total</th></tr></thead><tbody>';
      let sumaRepuestos = 0;
      reparacion.repuestos.forEach(r => {
        const total = r.cantidad * r.precio;
        sumaRepuestos += total;
        html += `<tr><td>${r.nombre}</td><td>${r.cantidad}</td><td>$${r.precio.toFixed(2)}</td><td>$${total.toFixed(2)}</td></tr>`;
      });
      html += '</tbody></table>';
      html += `<p><strong>Total repuestos:</strong> $${sumaRepuestos.toFixed(2)}</p>`;

      // Mano de obra - para simplicidad ponemos fija o 0
      const manoObra = reparacion.precioManoObra || 0;
      html += `<p><strong>Mano de obra:</strong> $${manoObra.toFixed(2)}</p>`;

      const totalFactura = sumaRepuestos + manoObra;
      html += `<h3>Total a pagar: $${totalFactura.toFixed(2)}</h3>`;
    }

    div.innerHTML = html;
  }

  // Consultar estado
  function consultarEstado(){
    const dni = document.getElementById('dniConsulta').value.trim();
    const div = document.getElementById('resultadoConsulta');
    div.innerHTML = '';

    if(!dni){
      div.textContent = 'Ingrese un DNI para la consulta.';
      return;
    }

    const vehiculosCliente = vehiculos.filter(v => v.clienteDni === dni);
    if(vehiculosCliente.length === 0){
      div.textContent = 'No se encontraron vehículos para ese DNI.';
      return;
    }

    let html = '<h3>Estado de reparaciones:</h3><ul>';
    vehiculosCliente.forEach(v => {
      const rep = reparaciones.find(r => r.vehiculoMatricula === v.matricula);
      if(rep){
        html += `<li>Vehículo ${v.matricula}: Estado - ${rep.estado}</li>`;
      } else {
        html += `<li>Vehículo ${v.matricula}: Sin reparación asignada.</li>`;
      }
    });
    html += '</ul>';
    div.innerHTML = html;
  }

</script>

</body>
</html>
