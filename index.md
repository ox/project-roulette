

  <style media="screen">
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    .sections * {
      display: inline-block;
    }

    .section {
      border: 1px dashed blue;
    }
  </style>

  <div class="container">
    <div class="machine">
      <div class="sections">
        <div>
          <span>Program a
            <a id="project"></a>
            with
            <a id="backend"></a>
            and
            <a id="frontend"></a>
          </span>
      </div>
      <div class="controls">
        <button id="play" onclick="window.spin()">Play Again</button>
      </div>
    </div>
  </div>

  <script type="text/javascript">
    const projects = [
      ['Todo App', 'http://todomvc.com/'],
      ['Text Editor', 'https://en.wikipedia.org/wiki/Text_editor'],
      ['Tetris', 'https://en.wikipedia.org/wiki/Tetris'],
      ['Ray Tracing Engine', 'https://en.wikipedia.org/wiki/Ray_tracing_(graphics)'],
      ['Calendar', 'https://calendar.google.com/'],
      ['Web Scraper', 'https://en.wikipedia.org/wiki/Web_scraping'],
      ['Uptime Checker', 'https://www.pingdom.com/'],
      ['Maze Generator', 'http://www.mazegenerator.net/'],
      ['Chat App', 'https://telegram.org/'],
      ['Flashcard App', 'https://www.ankiapp.com/'],
      ['Pomodoro Timer', 'https://en.wikipedia.org/wiki/Pomodoro_Technique'],
      ['IRC Clone', 'https://en.wikipedia.org/wiki/Internet_Relay_Chat'],
      ['Reaction Diffusion Simluator', 'https://en.wikipedia.org/wiki/Reaction%E2%80%93diffusion_system'],
      ['L-System Generator', 'https://en.wikipedia.org/wiki/L-system'],
      ['Project Roulette', '#'],
    ];

    const backends = [
      ['Go', 'https://golang.org/'],
      ['Clojure', 'https://clojure.org/'],
      ['C', 'https://www.programiz.com/c-programming'],
      ['Ada', 'https://www.adacore.com/about-ada'],
      ['Brainfuck', 'https://esolangs.org/wiki/Brainfuck'],
      ['Cobol', 'https://www.tutorialspoint.com/cobol/index.htm'],
      ['OCaml', 'https://ocaml.org/'],
      ['Reason', 'https://reasonml.github.io/'],
      ['Ruby', 'https://www.ruby-lang.org/en/'],
      ['Node.js', 'https://nodejs.org/en/'],
      ['Dino', 'https://github.com/dino-lang/dino'],
      ['Rust', 'https://www.rust-lang.org/'],
      ['Scala', 'https://www.scala-lang.org/'],
    ];

    const frontends = [
      ['React', 'https://reactjs.org/'],
      ['HTML + CSS', 'https://developer.mozilla.org/en-US/'],
      ['TelNet', 'https://tools.ietf.org/html/rfc854'],
      ['E-mail', 'https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol'],
      ['Command Line Interface', 'https://en.wikipedia.org/wiki/Command-line_interface'],
      ['iOS SDK', 'https://developer.apple.com/ios/'],
      ['Android SDK', 'https://developer.android.com/studio'],
      ['Flutter', 'https://flutter.dev/'],
    ];

    window.onload = () => {
      window.spin = () => {
        [['project', projects], ['backend', backends], ['frontend', frontends]].forEach(([target, choices]) => {
          const elem = document.getElementById(target);
          const [title, link] = choices[Math.floor(Math.random() * choices.length)];
          elem.href = link;
          elem.innerHTML = title;
        });
      };

      window.spin();
  }
  </script>
