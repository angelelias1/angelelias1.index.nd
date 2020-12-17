## Welcome to GitHub Pages

Puede usar el [editor en GitHub] (https://github.com/angelelias1/angelelias1.index.nd/edit/gh-pages/index.md) para mantener y obtener una vista previa del contenido de su sitio web en archivos Markdown.

si que se comprometa con este repositorio, las páginas de GitHub ejecutarán [Jekyll] ( https://jekyllrb.com/ ) para reconstruir las páginas de su sitio, a partir del contenido de sus archivos Markdown.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

rebaja
1. Numerado
2. Lista## Bienvenidos

## Que son las redes neuroanles
Las redes neuronales son redes interconectadas masivamente en paralelo de elementos simples y con organización jerárquica, las cuales intentan interactuar con los objetos del mundo real del mismo modo que lo hace el sistema nervioso biológico.

<img src="https://andromedavaluecapital.com/wp-content/uploads/2018/02/neuronal-network-1024x585.jpg" alt="Red neuronal">
## Cuál es su relacion con la tería de grafos
se relacionan porque los puntos neuronales estan conectados por las mismas aristas.

![Grafo](https://www.madrimasd.org/blogs/matematicas/files/2012/09/Network_representation_of_brain_connectivity.jpg)
<script src="https://www.gstatic.com/dialogflow-console/fast/messenger/bootstrap.js?v=1"></script>

<df-messenger
  intent="WELCOME"
  chat-title="Deber_Logica_Matematicas"
  agent-id="88185b68-d7e7-454c-ab0b-c8dceae0feb8"
  language-code="es"
></df-messenger>
<div>Teachable Machine Image Model</div>
<button type="button" onclick="init()">Start</button>
<div id="webcam-container"></div>
<div id="label-container"></div>
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@1.3.1/dist/tf.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@teachablemachine/image@0.8/dist/teachablemachine-image.min.js"></script>
<script type="text/javascript">
    // More API functions here:
    // https://github.com/googlecreativelab/teachablemachine-community/tree/master/libraries/image

    // the link to your model provided by Teachable Machine export panel
    const URL = "https://teachablemachine.withgoogle.com/models/_pAZQHuzk/";

    let model, webcam, labelContainer, maxPredictions;

    // Load the image model and setup the webcam
    async function init() {
        const modelURL = URL + "model.json";
        const metadataURL = URL + "metadata.json";

        // load the model and metadata
        // Refer to tmImage.loadFromFiles() in the API to support files from a file picker
        // or files from your local hard drive
        // Note: the pose library adds "tmImage" object to your window (window.tmImage)
        model = await tmImage.load(modelURL, metadataURL);
        maxPredictions = model.getTotalClasses();

        // Convenience function to setup a webcam
        const flip = true; // whether to flip the webcam
        webcam = new tmImage.Webcam(200, 200, flip); // width, height, flip
        await webcam.setup(); // request access to the webcam
        await webcam.play();
        window.requestAnimationFrame(loop);

        // append elements to the DOM
        document.getElementById("webcam-container").appendChild(webcam.canvas);
        labelContainer = document.getElementById("label-container");
        for (let i = 0; i < maxPredictions; i++) { // and class labels
            labelContainer.appendChild(document.createElement("div"));
        }
    }

    async function loop() {
        webcam.update(); // update the webcam frame
        await predict();
        window.requestAnimationFrame(loop);
    }

    // run the webcam image through the image model
    async function predict() {
        // predict can take in an image, video or canvas html element
        const prediction = await model.predict(webcam.canvas);
        for (let i = 0; i < maxPredictions; i++) {
            const classPrediction =
                prediction[i].className + ": " + prediction[i].probability.toFixed(2);
            labelContainer.childNodes[i].innerHTML = classPrediction;
        }
    }
</script>**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/angelelias1/angelelias1.index.nd/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

¿Tienes problemas con Pages? Consulte nuestra [documentación] ( https://docs.github.com/categories/github-pages-basics/ ) o [póngase en contacto con el servicio de asistencia] ( https://github.com/contact ) y lo ayudaremos un resolverlo afuera.
as
