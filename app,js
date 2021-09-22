console.log(document.querySelector('form'));
console.log(window.document.querySelector('form'));  //does the same but wondow. not needed window is inferred


const correctAnswers = ['B', 'B', 'B', 'B'];
const form = document.querySelector('.quiz-form');
const result = document.querySelector('.result');

form.addEventListener('submit', e => {
    e.preventDefault();

    let score = 0;
    const userAnswers = [form.q1.value, form.q2.value, form.q3.value, form.q4.value];
    

    // check answers
     userAnswers.forEach((answer, index) => {
        if (answer === correctAnswers[index]){
            score += 25;
        }
     });
        console.log(score);

    // show result on page, the ninja way
    scrollTo(0,0); //x-coordinate and y-coordinate
    //ninja puts the const=result in global scope above
    //result.querySelector('span').textContent = `${score}%`; //NOW COPIED TO THE INTERVAL, looks inside the scope of result for a spantag, then it we change the text equal to a template string of the score value
    result.classList.remove('d-none');

     let output = 0;
     const timer = setInterval(() => {
        result.querySelector('span').textContent = `${output}%`;
        if(output === score){
            clearInterval(timer);
        } else {
            output++;
        }
     }, 10);

});
