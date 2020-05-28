/* Help */

function log(message) {
  console.log(` > ${message}`);
}

const cards = document.querySelectorAll('.card');
const dropezones = document.querySelectorAll('.dropzone');

window.addEventListener('load', () => {
  start();
});

function start() {
  cards.forEach((card) => {
    card.addEventListener('dragstart', dragstart);
    card.addEventListener('drag', drag);
    card.addEventListener('dragend', dragend);
  });

  dropezones.forEach((dropzone) => {
    dropzone.addEventListener(`dragenter`, dragenter);
    dropzone.addEventListener(`dragover`, dragover);
    dropzone.addEventListener(`dragleave`, dragleave);
    dropzone.addEventListener(`drop`, drop);
  });
}

function dragstart() {
  dropezones.forEach((dropzone) => {
    dropzone.classList.add('highlight');
  });

  this.classList.add('is-draggin');
}

function drag() {
  log('Is Draggins');
}

function dragend() {
  dropezones.forEach((dropzone) => {
    dropzone.classList.remove('highlight');
  });

  this.classList.remove('is-draggin');
}

/*Local onde vou soltar os cartões*/

function dragenter() {
  log(`Dropzone? Enter in zone`);
}
function dragover() {
  //This é o dropzone
  this.classList.add('over');

  const cardBeingDragged = document.querySelector('.is-draggin');
  this.appendChild(cardBeingDragged);
}
function dragleave() {
  this.classList.remove('over');
}
function drop() {
  this.classList.remove('over');
}
