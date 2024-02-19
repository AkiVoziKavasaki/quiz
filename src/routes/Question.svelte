<script>
    export let question;
    export let correctAnswer;
    export let incorrectAnswer;

    let shuffle = (array) => array.sort(() => Math.random() - 0.5);
    let possibleAnswers = suffle([...incorrectAnswer,correctAnswer]);
    const handleClick = (answer) => {
        if (answer == correctAnswer){
            alert(`Tacno!`)
        }
        else{
            alert(`Netacno! Tacan odgovor je ${correctAnswer} `)
        }
    }
    </script>

    <div>
        <h3>{@html question}</h3>
        <div id="answer">
            <!-- Prikazi sve ponudjene odgovore kao button-e -->
            {#each possibleAnswers as pa, i}
                <button on:click={handleClick(i)}>{pa}</button>
            {/each}
        </div>
    </div>