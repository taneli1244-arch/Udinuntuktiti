


// 1. Initialize message index
let messageIndex = 0;

// 2. Define the messages that appear on the "No" button
const messages = [
    "Are you sure?",
    "Really sure?",
    "Think again!",
    "Last chance!",
    "Surely not?",
    "You might regret this!",
    "Are you absolutely sure?"
];

function handleNoClick() {
    const noButton = document.querySelector('.no-button');
    const yesButton = document.querySelector('.yes-button');

    // Change text on the 'no' button
    noButton.textContent = messages[messageIndex];
    
    // Cycle through messages, returning to 0 if at the end
    messageIndex = (messageIndex + 1) % messages.length;

    // Increase font size of the 'yes' button
    const currentSize = parseFloat(window.getComputedStyle(yesButton).fontSize);
    yesButton.style.fontSize = `${currentSize * 1.5}px`;
}

function handleYesClick() {
    // Redirect to a 'yes' page
    window.location.href = "yes_page.html";
}




