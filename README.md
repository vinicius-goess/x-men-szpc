// Leia os arquivos principais do projeto para inferir a finalidade e as tecnologias usadas
const mainFiles = ['index.html', 'style.css', 'app.js'];
const projectDetails = { description: '', technologies: [], usage: '' };

mainFiles.forEach(file => {
const filePath = path.join(__dirname, file);
if (fs.existsSync(filePath)) {
const content = fs.readFileSync(filePath, 'utf8');
if (file === 'index.html') {
// Extrai título e meta description se disponível
const titleMatch = content.match(/ <title> (.*?)</title>/);
if (titleMatch) projectDetails.description = titleMatch;
}
se (arquivo === 'style.css') {
projectDetails.technologies.push('CSS');
}
se (arquivo === 'app.js') {
projectDetails.technologies.push('JavaScript');
}
}
});

// Estrutura README base
const readme = `
