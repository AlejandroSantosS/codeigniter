<h1>CodeIgniter y el MVC</h1>


<p><b>Herramientas empleadas:</b> La herramienta principal sera Codeigniter como framework de desarrollo en servidor, apoyandose en bootstrap y jquery en el cliente</p>


<p><b>Aplicacion a desarrollar:</b> La aplicacion a desarrollar sera una tienda online, utilizando unicamente codeigniter y sus librerias para demostrar su potencia respecto a otros frameworks.</p>

<img src="http://blog.collectivecloudperu.com/wp-content/uploads/2015/04/111.png">

<h3>Temas a abordar en el proyecto</h1>

<ul>
  <li>¿Que es CI?</li>
  <li>Razones por las que usar CI como framework de desarrollo en servidor.</li>
  <li>Arquitectura MVC</li>
  <li>Pros y Contras del MVC</li>
  <li>Ventajas de usar CI</li>
  <li>Comparación de CI frente a otros</li>
  <li>Cracteristicas y potencia de CI</li>
  <li>Clases y librerias de CI</li>
  <li>Seguridad de CI</li>
  <li>CI en la comunidad de desarrolladores</li>
  <li>CI como framework back mas utilizado</li>
  <li>Aplicación de CI</li>
  <li>Otros...</li>
</ul>

<h3>Librerias utilizadas</h3>

Shopping Cart Class

<pre><code>
Para agregar un ítem al carrito, podemos utilizar un array multidimensional con la información del producto a la función $this- >cart->insert(), según se muestra aquí:

$data = array(
               array(
                       'id'      => 'sku_123ABC',
                       'qty'     => 1,
                       'price'   => 39.95,
                       'name'    => 'T-Shirt',
                       'options' => array('Size' => 'L', 'Color' => 'Red')
                    ),
               array(
                       'id'      => 'sku_567ZYX',
                       'qty'     => 1,
                       'price'   => 9.95,
                       'name'    => 'Coffee Mug'
                    ),
               array(
                       'id'      => 'sku_965QRS',
                       'qty'     => 1,
                       'price'   => 29.95,
                       'name'    => 'Shot Glass'
                    )
            );

$this->cart->insert($data);
</code></pre>


URL helper
<pre><code>
Por defecto, las URLs en CodeIgniter están diseñadas para ser amigable a los motores de búsqueda y amigables a los humanos. En vez de usar el estándar acercamiento "query string" para URLs que es sinónimo con sistemas dinámicos, CodeIgniter usa un aproximamiento basado-en-segmentos:

En este caso si tenemos una ruta http://github.com/codeigniter/alejandro
Obtendriamos la 3º posicion de la url.

$this->load->helper('url');

if ($this->uri->segment(3) === FALSE)
{
    $uriseg = 0;
}
else
{
    $uriseg = $this->uri->segment(3);
}
</code></pre>

Form Helper

El archivo del Helper Form contiene funciones que lo ayudan a trabajar con formularios. Ejemplo de formulario simple

<pre><code>$this->load->helper('form');
  echo form_open('email/send');
  echo form_input('name','value')
  echo form_submit('action','value')
</pre></code>


Calendaring Class

<pre><code>
Agregar datos a las celdas de tu calendario involucra crear un arreglo asociativo en el cual los índices corresponden a los días que desea llenar y el valor del arreglo contiene los datos. El arreglo es pasado al tercer parámetro de la función generar calendario. Considere este ejemplo:
$this->load->library('calendar');

$data = array(
               3  => 'http://example.com/news/article/2006/03/',
               7  => 'http://example.com/news/article/2006/07/',
               13 => 'http://example.com/news/article/2006/13/',
               26 => 'http://example.com/news/article/2006/26/'
             );

echo $this->calendar->generate(2006, 6, $data);
</code></pre>


Security Class

<pre><code> Codeigniter tiene una caracteristica muy importante y es que te protege contra el exploit CSRF y la vulnerabilidad XSS, ademas de evitar SQL injection.

Al ser uno de los temas mas complejos se abordara principalmente en la presentacion</pre></code>




Config Class


<pre><code>
Por defecto, CodeIgniter tiene un archivo primario de configuracion, ubicado en application/config/config.php. Si abres un archivo usando tu editor de texto verás que los items son almacenados en un arreglo llamado $config.

Puedes agregar tus propios items de configuración a este archivo, o si lo prefieres, puedes mantenerlos en forma separada (asumiendo que necesitas items de configuración), simplemente debes crear tu archivo de configuración y guardarlo en la carpeta config.

$this->config->load('nombre_archivo')</pre></code>

Caching Driver

<pre><code>
En el ejemplo siguiente se carga el controlador de memoria caché, APC como driver a utilizar, y cambia a almacenamiento en caché basado en archivo si APC no está disponible en el entorno de alojamiento.
$this->load->driver('cache', array('adapter' => 'apc', 'backup' => 'file'));

if ( ! $foo = $this->cache->get('foo'))
{
        echo 'Saving to the cache!<br />';
        $foo = 'foobarbaz!';

        // Save into the cache for 5 minutes
        $this->cache->save('foo', $foo, 300);
}

echo $foo;
</code></pre>

<h4>Otras clases y librerias utilizadas</h4>

<b>Encrypt Class</b>(Muy importante)<br>
<b>Encryption Library</b>(Muy importante)<br>
File Uploading Class<br>
<b>Form Validation</b>(Muy importante)<br>
FTP Class<br>
Image Manipulation Class<br>
Input Class<br>
Javascript Class<br>
Language Class<br>
Loader Class<br>
Output Class<br>
<b>Pagination Class</b> (Muy importante)<br>
Template Parser Class<br>
<b>Session Library</b> (Muy importante)<br>
HTML Table Class
Trackback Class
Typography Class
Unit Testing Class
<b>URI Class</b> (Muy importante)<br>
User Agent Class
XML-RPC and XML-RPC Server Classes
Zip Encoding Class

<h4>Esto solo es un muy pequeño ejemplo de algunas lineas de codigo de CI, las librerias utilizas que no añado codigo demo simplemente es para no saturar la web de información. La aplicacion que estoy desarrollando es mucho mas compleja de lo que puedo mostrar aqui, para mas informacion podeis enviar un correo a alexdevop@gmail.com</h4>
