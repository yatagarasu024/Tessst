function showStars() {
    const card = document.querySelector('.card');

    for (let i = 0; i < 20; i++) {
        const star = document.createElement('div');
        star.innerHTML = '★';
        star.className = 'star';
        star.style.top = `${Math.random() * 100}%`;
        star.style.left = `${Math.random() * 100}%`;
        card.appendChild(star);
    }

    setTimeout(() => {
        const stars = document.querySelectorAll('.star');
        stars.forEach(star => star.remove());
    }, 2000);
}