<a id="readme-top"></a>
<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/github_username/repo_name">
    <img src="logo.png" alt="Logo" width="80" height="80">
  </a>

  # Unblocked Games Kit
everything you need for the school year  
A collection of playable HTML5 games that bypass school game blockers. This project compiles open-source games from various HTML5 libraries into standalone `.html` files that can't be blocked by traditional network filters.

## Download

<div style="margin: 20px 0;">
  <button onclick="openInBlank()" style="padding: 10px 20px; font-size: 16px; background-color: #0969da; color: white; border: none; border-radius: 6px; cursor: pointer;">Open Game in Blank Tab</button>
  <input type="text" id="filePath" placeholder="Enter file path (e.g., index.html)" style="padding: 10px; margin-left: 10px; border: 1px solid #ccc; border-radius: 4px; width: 250px;">
</div>

<script>
function openInBlank() {
  const filePath = document.getElementById('filePath').value || 'index.html';
  const owner = 'Jo-Nathan-1';
  const repo = 'Unblocked-GamesKit';
  const branch = 'main';
  const url = `https://raw.githubusercontent.com/${owner}/${repo}/${branch}/${filePath}`;
  
  fetch(url)
    .then(r => {
      if (!r.ok) throw new Error('File not found');
      return r.text();
    })
    .then(html => {
      const w = window.open('about:blank');
      w.document.write(html);
      w.document.close();
    })
    .catch(err => alert('Error: ' + err.message + '\nMake sure the file path is correct.'));
}
</script>

## Features

- **Unblockable**: Pure HTML/CSS/JavaScript games that work around school network filters
- **Diverse Game Library**: Includes popular titles like Cuphead, Bad Piggies, Angry Birds, and the entire gn-math library
- **Open Source**: Built from various open-source HTML5 game libraries
- **Easy to Use**: Just open the `.html` files in any browser

## Games and libraries
- [gams](https://github.com/Gams-Offline/Gams) 

- All open-source game libraries and creators
- HTML5 game development community
- gn-math for the unblocked games and web ports library

<p align="right">(<a href="#readme-top">back to top</a>)</p>
