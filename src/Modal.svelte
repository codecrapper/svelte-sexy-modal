<script>
    export let modalIsOpen
    export let modalHeader = "TITLE: 💩 Denny an cuc 💩"
    export let modalContent = "But we're not there yet, so we don't need to worry about it. In life you need colors. If what you're doing doesn't make you happy - you're doing the wrong thing. I guess I'm a little weird. I like to talk to trees and animals. That's okay though; I have more fun than most people. No worries. No cares. Just float and wait for the wind to blow you around. We'll throw some old gray clouds in here just sneaking around and having fun."
    export let modalCloseButton = "Close Modal"
    export let modalStylingOverlay
    export let modalStyling

    const modalClose = () => {
        modalIsOpen = false;
    }
    
</script>

<div class="modal-container">
    {#if modalIsOpen}
        <div>
            <div class="overlay-style" on:click={modalClose} style={modalStylingOverlay}></div>
            <div class="modal-wrapper" style={modalStyling}>
                <div class="modal-header">
                    <h3 class="modal-title">{modalHeader}</h3>
                    <span class="close-modal-x" on:click={modalClose}>x</span>
                </div>
                <hr />
                <div class="modal-content">
                    <div class="modal-body">
                        <p>{modalContent}</p>
                    </div>
                    <div class="modal-footer">
                        <button class="close-modal-button" on:click={modalClose}>{modalCloseButton}</button>
                    </div>
                </div>
            </div>
        </div>
    {/if}
  </div>

<style>

    * {
        box-sizing: border-box;
    }

    .modal-container {
        font-family: Arial, Helvetica, sans-serif;
        position: relative;
        z-index:  1;
    }

    .overlay-style {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: rgba(0, 0, 0, 0.7);
        z-index: 1000;
    }

    .modal-wrapper {
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background-color: #FFF;
        padding: 35px 50px;
        z-index: 1000;
    }

    .modal-header {
        margin: 0;
        padding: 0;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .close-modal-x {
        font-size: 1.3rem;
        color: #808080;
    }

    .close-modal-x:hover {
        color: #3a3737;
    }

    .close-modal-x, .close-modal-button {
        cursor: pointer;
    }
</style>