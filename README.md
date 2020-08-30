What's crackin'

## Installation 
```
$ npm install svelte-sexy-modal --save
```

## Usage
```
	<script>
        import Modal from '../node_modules/svelte-sexy-modal'

        let modalIsOpen = true

        const openModal = () => {
            modalIsOpen = true
        }
    </script>

	<button on:click={openModal}>Open modal</button>
    <Modal bind:modalIsOpen={modalIsOpen} />

```

1. Props
	```
	let modalIsOpen = {boolean}
    let modalHeader 
    let modalContent 
    let modalCloseButton 
    let modalStylingOverlay
    let modalStyling
	
	```