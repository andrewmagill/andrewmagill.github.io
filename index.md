<!doctype html>
<html>
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">

    <title>Gateways 2020 Demo: Geoweaver</title>
    <meta name="author" content="Andrew Magill">

    <link rel="stylesheet" href="lib/tabzilla/css/tabzilla.css"/>
    <link rel="stylesheet" href="lib/reveal/css/reveal.css"/>
    <link rel="stylesheet" href="lib/reveal/css/theme/mozilla-devrel-light.css"/>

		<!-- Theme used for syntax highlighting of code -->
    <link rel="stylesheet" href="lib/reveal/lib/css/solarized-light.css" />

    <style type="text/css">
        /* https://github.com/hakimel/reveal.js/issues/806#issuecomment-222417787 */
        /* 1. Style header/footer <div> so they are positioned as desired. */
        header {
        }
        #header-left {
            position: absolute;
            top: 0%;
            left: 0%;
            width: 100%;
            font-size: 24px;
            text-align: center;
            color: rgb(245, 244, 236);
            background-color: #484848;
        }
        #header-right {
            position: absolute;
            top: 0%;
            right: 0%;
            width: 50%;
            background-color: #484848;
        }
        #footer-left {
            position: absolute;
            bottom: 0%;
            left: 0%;
        }
    </style>

		<!-- Printing and PDF exports -->
		<script>
			var link = document.createElement( 'link' );
			link.rel = 'stylesheet';
			link.type = 'text/css';
      link.href = window.location.search.match( /print-pdf/gi ) ? 'lib/reveal/css/print/pdf.css' : 'lib/reveal/css/print/paper.css';
			document.getElementsByTagName( 'head' )[0].appendChild( link );
		</script>
	</head>
  <body>

    <!-- 2. Create hidden header/footer <div> -->
    <div id="hidden" style="display:none;">
        <div id="header">
            <div id="header-left">Gateways 2020: Geoweaver</div>
            <div id="header-right"></div>
            <div id="footer-left"></div>
        </div>
    </div>

		<div class="reveal">
			<div class="slides">
        <section>
          <header>
            <h1>Geoweaver</h1>
            <p>Manage process workflows and provenance across distributed resources</p>
          </header>
        </section>

        <section>
          <ol>
            <li>What is Geoweaver?</li>
            <li>How does it work?</li>
            <li>What makes Geoweaver unqiue?</li>
            <li>Future work</li>
            <li>Acknowledgments</li>
            <li>Questions</li>
          </ol>
        </section>

        <section>
          <section>
            <h2>What is Geoweaver?</h2>
          </section>

          <section>
            <img style="max-height: 500px;" alt="Geoweaver screenshot" src="./imgs/geoweaver_hero.png" />
            <p>
              <a href="https://github.com/delapuente/pangolink" target="_blank">Geoweaver</a>
            is a web base plaform that enables you to manage your deep learning workflows and provenance across distributed resources.</a>
            </p>
          </section>

        </section>

        <section>
          <section>
            <h2>How does it work?</h2>
          </section>

          <section>
            <video style="max-height: 550px;" data-autoplay src="video/create_ssh_host.mp4"></video>
            <p>
              In Geoweaver, hosts are the resources where we run our processes. Here we are registering a machine that we connect to through SSH.
            </p>
          </section>

          <section>
            <video style="max-height: 550px;" data-autoplay src="video/create_jupyter_host_2.mp4"></video>
            <p>
              We can also add Jupyter Servers as host resources, allowing us to interact with and edit our workflow processes.
            </p>
          </section>

          <section>
            <video style="max-height: 550px;" data-autoplay src="video/create_bash_process_4.mp4"></video>
            <p>
            We can add a variety of different types of processes, here we are adding a bash script that will download imagery prior to processing.
            </p>
          </section>

          <section>
            <video style="max-height: 550px;" data-autoplay src="video/create_jupyter_process.mp4"></video>
            <p>
            And we can upload or import Jupyter notebooks.
            </p>
            <p><small>Jupyter Notebook source: <a href="https://www.earthdatascience.org/courses/use-data-open-source-python/multispectral-remote-sensing/landsat-in-Python/replace-raster-cell-values-in-remote-sensing-images-in-python/">Intermediate Earth Data Science Textbook</a>, an online course provided by Earth Lab CU Boulder at <a hred="https://www.earthdatascience.org/">earthdatascience.org</a></small></p>
          </section>

          <section>
            <video style="max-height: 550px;" data-autoplay src="video/process_results_and_file_listing.mp4"></video>
            <p>
            Geoweaver stores a detailed history of every process we have run, we can view the logs, and examine outputs on the server.
            </p>
          </section>

          <section>
            <video style="max-height: 550px;" data-autoplay src="video/create_workflow.mp4"></video>
            <p>
            Processes can be linked together to form workflows, so that we can run our processes in parallel or sequentially across separate resources, and manage it all in one place.
            </p>
          </section>

        </section>

        <section>
          <section>
            <h2>What makes Geoweaver unique?</h2>
          </section>

          <section>
            <video style="max-height: 550px;" data-autoplay src="video/versioned_jupyter_notebook.mp4"></video>
            <p>
            Geoweaver intercepts websocket traffic between you and your Jupyter Server, saving versions of your notebook as you edit, allowing you to return to previous states.
            </p>
          </section>
        </section>

        <section>
          <section>
            <h2>Future work</h2>
          </section>

          <section>
            <iframe width="850" height="550" src="https://earthengine.google.com/" frameborder="0" allowfullscreen></iframe>
            <p>
            We are developing support for Google Earth Engine as a Geoweaver host resource.
            </p>
          </section>
        </section>

        <section>
          <h2>Acknowledgements</h2>
          <ul>
            <li>The following organizations have provided funding and support for the development of Geoweaver: 
              <p>
                <small>
                  <a href="https://www.esipfed.org/">ESIPFed</a>
                  <img style="width: 100px; margin-top: -10px; margin-left: 10px; margin-right: 10px"src="https://www.esipfed.org/wp-content/uploads/2019/09/esip-logo-uptodate.transparent-background.png"/>
                  <a href="https://sciencegateways.org/">SGCI</a>
                  <img style="height: 51px; background-color: rgb(60,62,63); margin-top: -10px; margin-left: 10px; margin-right: 10px"src="https://sciencegateways.org/sciencegateways-theme/images/sgci-logos/sgci-new-logo-words-horiz-white.png"/>
                  <a href="https://earthdata.nasa.gov/">NASA</a>
                  <img style="height: 51px; background-color: rgb(70,113,163); margin-top: -10px; margin-left: 10px;"src="https://earthdata.nasa.gov/img/nasa-logo.png"/>
                </small>
              </p></li>
            <li>The following individuals have contributed to the project:
              <small>
              <p>Ziheng Sun, Center for Spatial Information Science and Systems, George Mason University</p>
              <p>Liping Di,  Center for Spatial Information Science and Systems, George Mason University</p>
              <p>Annie Burgess, Earth Science Information Partners (ESIP)</p>
              <p>Jason A. Tullis, Department of Geosciences and Center for Advanced Spatial Technologies, University of Arkansas</p>
              <p>Andrew Magill, Texas Advanced Computing Center, The University of Texas at Austin</p>
              </small>
            </li>
          </ul>
        </section>

        <section>
          <p>Contact</p>
          <p><a href="mailto:zsum@gmu.edu">Ziheng Sun: zsun@gmu.edu</a></p>
          <p><a href="mailto:amagill@tacc.utexas.edu">Andrew Magill: amagill@tacc.utexas.edu</a></p>
          <p><a href="https://esipfed.github.io/Geoweaver/">https://esipfed.github.io/Geoweaver/</a></p>
        </section>

        <section data-markdown>
          ## Questions?
        </section>
      </div>
		</div>

    <script src="lib/reveal/lib/js/head.min.js"></script>
    <script src="lib/reveal/js/reveal.js"></script>

    <script>
      // More info https://github.com/hakimel/reveal.js#configuration
			Reveal.initialize({
				history: true,

				// More info https://github.com/hakimel/reveal.js#dependencies
				dependencies: [
          { src: 'lib/reveal/plugin/markdown/marked.js' },
          { src: 'lib/reveal/plugin/markdown/markdown.js' },
          { src: 'lib/reveal/plugin/notes/notes.js', async: true },
          { src: 'lib/reveal/plugin/highlight/highlight.js', async: true, callback: function() { hljs.initHighlightingOnLoad(); } }
				]
			});
		</script>

    <script src="https://code.jquery.com/jquery-2.2.4.min.js"></script>

    <script type="text/javascript">
        /* https://github.com/hakimel/reveal.js/issues/806#issuecomment-222417787 */
        // 3. On Reveal.js ready event, copy header/footer <div> into each `.slide-background` <div>
        var header = $('#header').html();
        if ( window.location.search.match( /print-pdf/gi ) ) {
            Reveal.addEventListener( 'ready', function( event ) {
                $('.slide-background').append(header);
            });
        }
        else {
            $('div.reveal').append(header);
       }
    </script>
	</body>
</html>
