<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Electromagnetismo en Electroterapia Médica</title>
    <style>
        /* Estilos generales */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Encabezado */
        header {
            background: linear-gradient(135deg, #1a5f7a, #2a7ca6);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        /* Navegación */
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 0.5rem 0.8rem;
            border-radius: 4px;
            transition: background-color 0.3s;
        }
        
        nav ul li a:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        /* Sección Hero */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), 
                        url('https://images.unsplash.com/photo-1559757148-5c350d0d3c56?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 5rem 0;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
        }
        
        /* Secciones */
        section {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: #1a5f7a;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #2a7ca6;
            margin: 0.5rem auto;
            border-radius: 2px;
        }
        
        /* Perfiles */
        .profiles-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .profile-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .profile-card:hover {
            transform: translateY(-5px);
        }
        
        .profile-img {
            height: 200px;
            background-color: #e0e0e0;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #777;
        }
        
        .profile-info {
            padding: 1.5rem;
        }
        
        .profile-name {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #1a5f7a;
        }
        
        .profile-program {
            color: #666;
            font-style: italic;
        }
        
        /* Descripción del proyecto */
        .project-description {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .project-description h3 {
            color: #1a5f7a;
            margin-bottom: 1rem;
            margin-top: 1.5rem;
        }
        
        .project-description h3:first-child {
            margin-top: 0;
        }
        
        .project-description p {
            margin-bottom: 1.5rem;
        }
        
        .project-description ul {
            margin-left: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .project-description li {
            margin-bottom: 0.5rem;
        }
        
        /* Estado del arte */
        .research-content {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            line-height: 1.5;
            font-size: 12pt;
        }
        
        .subtopic {
            margin-bottom: 2.5rem;
        }
        
        .subtopic h3 {
            color: #1a5f7a;
            margin-bottom: 1rem;
            border-bottom: 2px solid #e0e0e0;
            padding-bottom: 0.5rem;
        }
        
        .highlight {
            background-color: #e3f2fd;
            padding: 0.2rem 0.4rem;
            border-radius: 3px;
            font-weight: 600;
        }
        
        .equation {
            background-color: #f5f5f5;
            padding: 1rem;
            border-radius: 5px;
            margin: 1rem 0;
            font-family: 'Courier New', monospace;
            text-align: center;
            border-left: 4px solid #2a7ca6;
        }
        
        .diagram {
            max-width: 100%;
            margin: 1.5rem auto;
            display: block;
            border-radius: 5px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
        }
        
        .application-box {
            background-color: #e8f4f8;
            border-radius: 8px;
            padding: 1.5rem;
            margin: 1.5rem 0;
            border-left: 4px solid #1a5f7a;
        }
        
        .application-title {
            color: #1a5f7a;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }
        
        /* Pie de página */
        footer {
            background-color: #1a5f7a;
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
        }
        
        /* Diseño responsivo */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 0.5rem;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Encabezado -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">Electromagnetismo en Medicina</div>
                <nav>
                    <ul>
                        <li><a href="#profiles">Perfiles</a></li>
                        <li><a href="#project">Descripción</a></li>
                        <li><a href="#research">Fundamentos</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Sección Hero -->
    <section class="hero">
        <div class="container">
            <h1>Electromagnetismo en Electroterapia Médica</h1>
            <p>El objetivo es conectar los principios físicos con aplicaciones médicas para el manejo del dolor y la rehabilitación</p>
        </div>
    </section>

    <!-- Perfiles -->
    <section id="profiles">
        <div class="container">
            <h2 class="section-title">Perfiles del Equipo</h2>
            <div class="profiles-grid">
                <!-- Perfil 1 -->
                <div class="profile-card">
                    <img class="profile-img" src="C:\Users\ACER-PC\Downloads\WhatsApp Image 2025-11-06 at 4.07.10 AM.jpeg" alt="Foto del integrante">
                    <div class="profile-info">
                        <h3 class="profile-name">Juanita Castañeda Bustamante</h3>
                        <p class="profile-program">Ingenieria Física</p>
                    </div>
                </div>
                
                
            </div>
        </div>
    </section>

    <!-- Descripción del proyecto -->
    <section id="project">
        <div class="container">
            <h2 class="section-title">Descripción del Proyecto</h2>
            <div class="project-description">
                <h3>Objetivo General</h3>
                <p>Se busca demostrar de manera teórica cómo los principios fundamentales del electromagnetismo (vistos en Física 2) son la base de técnicas médicas de electroterapia ampliamente utilizadas en la actualidad para el manejo del dolor, la rehabilitación muscular y la estimulación neuronal.</p>
                
                <h3>Planteamiento del Problema</h3>
                <p>Existe una brecha entre la teoría electromagnética (leyes de Ohm, Faraday, campos electromagnéticos) y sus aplicaciones prácticas en la vida cotidiana. Este proyecto busca cerrar esa brecha, mostrando cómo estas leyes físicas se materializan en dispositivos médicos que mejoran la salud y la calidad de vida de las personas.</p>
                
                <h3>Aplicaciones de la Electroterapia a Investigar</h3>
                <ul>
                    <li><strong>TENS (Estimulación Eléctrica Nerviosa Transcutánea):</strong> Es cuando se hace uso de corriente de baja frecuencia para el manejo del dolor badado en la Teoría de la Compuerta la cual explica que la médula espinal tiene un sistema de "compuertas" que regulan el paso de las señales de dolor al cerebro.</li>
                    <li><strong>EMS (Estimulación Eléctrica Muscular):</strong> Se hace uso de corriente para generar contracciones musculares y prevenir la atrofia.</li>
                    <li><strong>Magnetoterapia:</strong> Aplicación de campos electromagnéticos pulsados o CEMP el cual sirve para estimular la regeneración de tejidos, especialmente en el caso de fracturas óseas.</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Estado del arte -->
    <section id="research">
        <div class="container">
            <h2 class="section-title">Fundamentos Físicos y Estado del Arte</h2>
            <div class="research-content">
                <!-- Subtema 1 -->
                <div class="subtopic">
                    <h3>Corriente Eléctrica en Tejidos Biológicos</h3>
                    <p>Los tejidos biológicos presentan propiedades eléctricas complejas que determinan cómo responden a la corriente eléctrica aplicada. A diferencia de los conductores metálicos, los tejidos biológicos exhiben tanto propiedades resistivas como capacitivas, lo que se describe mediante el concepto de <span class="highlight">impedancia</span>.</p>
                    
                    <p>La Ley de Ohm adaptada para tejidos biológicos se expresa como:</p>
                    
                    <div class="equation">V = I × Z</div>
                    
                    <p>Donde V es el voltaje aplicado, I es la corriente que fluye a través del tejido, y Z es la impedancia del tejido. La impedancia es la oposición que presenta un tejido al paso de una corriente eléctrica ydepende de la frecuencia de la corriente aplicada, la composición del tejido y su hidratación.</p>
                    
                    <p>En electroterapia, es fundamental medir la <span class="highlight">impedancia tisular</span> para determinar los parámetros óptimos de tratamiento. La impedancia se calcula como:</p>
                    
                    <div class="equation">Z = √(R² + Xc²)</div>
                    
                    <p>Donde R es la resistencia y Xc es la reactancia capacitiva que es la oposición que presenta un condensador al flujo de corriente alterna .</p>
                    
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Biological_tissue_impedance_model.svg/500px-Biological_tissue_impedance_model.svg.png" alt="Modelo de impedancia en tejidos biológicos" class="diagram">
                </div>
                
                <!-- Subtema 2 -->
                <div class="subtopic">
                    <h3>Tipos de Corriente y sus Efectos Fisiológicos</h3>
                    <p>En electroterapia se utilizan principalmente dos tipos de corriente: continua (galvánica) y alterna, cada una con efectos fisiológicos distintos.</p>
                    
                    <p>La <span class="highlight">corriente continua</span> mantiene una polaridad constante, lo que genera efectos electroquímicos significativos en los tejidos. La densidad de corriente (J) es un parámetro crucial que se calcula como:</p>
                    
                    <div class="equation">J = I / A</div>
                    
                    <p>Donde I es la corriente y A es el área de aplicación. Este parámetro determina la intensidad del estímulo en el tejido.</p>
                    
                    <p>La <span class="highlight">corriente alterna</span>, por su parte, cambia de dirección periódicamente, lo que reduce los efectos electroquímicos pero permite una mayor penetración en el tejido. La frecuencia de la corriente alterna determina sus efectos fisiológicos, y estos son:</p>
                    
                    <ul>
                        <li>Bajas frecuencias (1-10 Hz): Estimulación nerviosa</li>
                        <li>Medias frecuencias (10-100 Hz): Contracción muscular</li>
                        <li>Altas frecuencias (>100 Hz): Efectos analgésicos</li>
                    </ul>
                    
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7a/Waveforms.svg/600px-Waveforms.svg.png" alt="Formas de onda en electroterapia" class="diagram">
                </div>
                
                <!-- Subtema 3 -->
                <div class="subtopic">
                    <h3>Inducción Electromagnética en Aplicaciones Médicas</h3>
                    <p>La Ley de Faraday establece que un campo magnético variable en el tiempo induce una fuerza electromotriz (FEM) en un conductor, el cual es el trabajo por unidad de carga que se genera en un circuito conductor debido a un cambio en el flujo magnético a través de él. En el contexto médico, los tejidos biológicos actúan como conductores, permitiendo que campos magnéticos externos induzcan corrientes internas.</p>
                    
                    <p>La Ley de Faraday se expresa como:</p>
                    
                    <div class="equation">ε = -dΦ<sub>B</sub>/dt</div>
                    
                    <p>Donde ε es la fuerza electromotriz inducida y Φ<sub>B</sub> es el flujo magnético. En aplicaciones médicas, el flujo magnético se calcula como:</p>
                    
                    <div class="equation">Φ<sub>B</sub> = B × A × cosθ</div>
                    
                    <p>Donde B es la densidad de flujo magnético, A es el área de la espira (tejido) y θ es el ángulo entre el campo magnético y la normal al área.</p>
                    
                    <p>En la Estimulación Magnética Transcraneal (TMS), se utilizan pulsos magnéticos rápidos para inducir corrientes en regiones específicas del cerebro, permitiendo el estudio y tratamiento de trastornos neurológicos.</p>
                    
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d3/Transcranial_magnetic_stimulation.jpg/600px-Transcranial_magnetic_stimulation.jpg" alt="Estimulación Magnética Transcraneal" class="diagram">
                </div>
                
                <!-- Aplicaciones -->
                <div class="subtopic">
                    <h3>Aplicaciones Específicas de Electroterapia</h3>
                    
                    <div class="application-box">
                        <div class="application-title">TENS (Estimulación Eléctrica Nerviosa Transcutánea)</div>
                        <p>Utiliza corrientes de baja frecuencia (2-150 Hz) y baja intensidad para activar fibras nerviosas aferentes, bloqueando la transmisión de señales de dolor según la Teoría de la Compuerta de Melzack y Wall anteriormente explicada. Los parámetros clave incluyen:</p>
                        <img src="C:\Users\ACER-PC\OneDrive.JPNG" alt="TENS" class="diagram" name="TENS">
                        <ul>
                            <li><span class="highlight">Frecuencia:</span> 2-150 Hz (modulable)</li>
                            <li><span class="highlight">Ancho de pulso:</span> 50-200 μs</li>
                            <li><span class="highlight">Intensidad:</span> Hasta 60 mA (por debajo del umbral de contracción muscular)</li>
                        </ul>
                    </div>
                    
                    <div class="application-box">
                        <div class="application-title">EMS (Estimulación Eléctrica Muscular)</div>
                        <p>Aplica corrientes para generar contracciones musculares mediante la despolarización de membranas de motoneuronas, el cual es el proceso por el cual se genera una señal nerviosa en el cerebro. Se utiliza para:</p>
                        <ul>
                            <li>Prevención de atrofia muscular</li>
                            <li>Rehabilitación post-lesión</li>
                            <li>Entrenamiento muscular en atletas</li>
                        </ul>
                        <p>Los parámetros típicos incluyen frecuencias de 20-50 Hz y anchos de pulso de 200-400 μs.</p>
                    </div>
                    
                    <div class="application-box">
                        <div class="application-title">Magnetoterapia</div>
                        <p>Aplica campos electromagnéticos pulsados de baja frecuencia (1-100 Hz) y baja intensidad (1-100 G) para estimular procesos de regeneración tisular. Sus efectos incluyen:</p>
                        <ul>
                            <li>Aceleración de la consolidación ósea en fracturas</li>
                            <li>Reducción de la inflamación</li>
                            <li>Estimulación de la angiogénesis</li>
                        </ul>
                        <p>La densidad de flujo magnético (B) la cual es la cantidad de líneas de campo magnético que pasan a través de una área especifica y es un parámetro crítico que se mide en Gauss (G) o Tesla (T).</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pie de página -->
    <footer>
        <div class="container">
            <p>Proyecto: Electromagnetismo en Electroterapia Médica</p>
            <p>Física 2 - Universidad</p>
        </div>
    </footer>
</body>
</html>
