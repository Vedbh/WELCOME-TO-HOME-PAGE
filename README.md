<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Code Display</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        .logo-container {
            display: flex;
            justify-content: space-around;
            padding: 20px;
        }

        .logo {
            width: 100px;
            height: 100px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            font-weight: bold;
            color: #000;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            cursor: pointer;
            background-color: silver;
        }

        .code-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: none;
            background-color: rgba(255, 255, 255, 0.9);
            padding: 20px;
            box-sizing: border-box;
            white-space: pre-wrap;
            font-family: monospace;
        }
    </style>
</head>
<body>
    <main>
        <div class="logo-container">
            <div class="logo" onclick="showCode('js-code-container')">JS</div>
            <div class="logo" onclick="showCode('html-code-container')">HTML</div>
            <div class="logo" onclick="showCode('css-code-container')">CSS</div>
            
            <!-- JavaScript Code Container -->
            <div id="js-code-container" class="code-container">
                <button onclick="hideCode('js-code-container')">Hide Code</button>
                <h3>JavaScript Code:</h3>
                <pre>
                    function showCode(containerId) {
                        document.getElementById(containerId).style.display = 'block';
                        hideOtherCodeContainers(containerId);
                    }
                   
                </pre>
            </div>

            <!-- HTML Code Container -->
            <div id="html-code-container" class="code-container">
                <button onclick="hideCode('html-code-container')">Hide Code</button>
               
                <h3>HTML Code:</h3>
                <pre>
                   
                    <header>
                        <h1>Welcome to My HTML Page</h1>
                    </header>
                
                    <main>
                        <p>This is a sample HTML content. Modify and add your own elements here.</p>
                    </main>
                
                    <footer>
                        <p>&copy; 2023 Ved Website </p>
                    </footer>
                   </pre>
                
            </div>

            <!-- CSS Code Container -->
            <div id="css-code-container" class="code-container">
                <button onclick="hideCode('css-code-container')">Hide Code</button>
                <h3>CSS Code:</h3>
                <pre>
                    .code-container {
                        position: absolute;
                        top: 0;
                        left: 0;
                        width: 100%;
                        height: 100%;
                        display: none;
                        background-color: rgba(255, 255, 255, 0.9);
                        padding: 20px;
                        box-sizing: border-box;
                        white-space: pre-wrap;
                        font-family: monospace;
                    }
                </pre>
            </div>
        </div>
    </main>

    <script>
        function showCode(containerId) {
            document.getElementById(containerId).style.display = 'block';
            hideOtherCodeContainers(containerId);
        }

        function hideCode(containerId) {
            document.getElementById(containerId).style.display = 'none';
        }

        function hideOtherCodeContainers(exceptContainerId) {
            const containerIds = ['js-code-container', 'html-code-container', 'css-code-container'];
            containerIds.forEach(id => {
                if (id !== exceptContainerId) {
                    document.getElementById(id).style.display = 'none';
                }
            });
        }
    </script>
</body>
</html>
<ul></ul>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML, CSS, and JavaScript Example</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 100px;
            background-color: #f4f4f4;
            text-align: center;
        }

        header {
            background-color: #333;
            color: white;
            padding: 1em;
            text-align: center;
        }

        section {
            margin: 20px;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        #colorChangeButton {
            padding: 10px;
            font-size: 16px;
            cursor: pointer;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #4CAF50;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        pre{
            color: blue;
        }
        footer {
    background-color: #333;
    color: white;
    padding: 10px;
    text-align: center;
    position: fixed;
    bottom: 0;
    width: 100%;
}
       </style>

    <header>
        <h1>HTML, CSS, and JavaScript Language </h1>
    </header>

    <section>
        <h2>HTML LANGUAGE</h2>
        <p>HTML (HyperText Markup Language) is the standard markup language for creating web pages. It provides the structure of the content on the web page using a system of elements and attributes.</p>
        <p>Example:</p>
        <pre>
            <code>
                &lt;html&gt;
                    &lt;head&gt;
                        &lt;title&gt;My Web Page&lt;/title&gt;
                    &lt;/head&gt;
                    &lt;body&gt;
                        &lt;h1&gt;Hello, World!&lt;/h1&gt;
                    &lt;/body&gt;
                &lt;/html&gt;
            </code>
        </pre>
    </section>

    <section>
        <h2>CSS LANGUAGE</h2>
        <p>CSS (Cascading Style Sheets) is used for styling the visual presentation of a web page written in HTML. It allows you to control the layout, colors, and fonts of your HTML elements.</p>
        <p>Example:</p>
        <pre>
            <code>
                body {
                    font-family: 'Arial', sans-serif;
                    background-color: #f4f4f4;
                }

                h1 {
                    color: #333;
                }
            </code>
        </pre>
    </section>

    <section>
        <h2>JavaScript Language</h2>
        <p>JavaScript is a programming language that enables interactive web pages. It can be used to manipulate the content and behavior of a web page, making it dynamic and responsive.</p>
        <p>Example:</p>
        <pre>
            <code>
                function changeColor() {
                    document.body.style.backgroundColor = '#87CEEB';
                }
                function changeColor() {
                    document.body.style.backgroundColor = getRandomColor();
                }
            
                function getRandomColor() {
                    var letters = '0123456789ABCDEF';
                    var color = '#';
                    for (var i = 0; i < 6; i++) {
                        color += letters[Math.floor(Math.random() * 16)];
                    }
                    return color;
                }
            </code>
        </pre>
        <button onclick="changeColor()">Click me</button>

    </section>
    <footer>
        WEB DESIGNER : VED BHOGAYTA
    </footer>
<script>
    function changeColor() {
        document.body.style.backgroundColor = getRandomColor();
    }

    function getRandomColor() {
        var letters = '0123456789ABCDEF';
        var color = '#';
        for (var i = 0; i < 6; i++) {
            color += letters[Math.floor(Math.random() * 16)];
        }
        return color;
    }
</script>
</body>
</html>
