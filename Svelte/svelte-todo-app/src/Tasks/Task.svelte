<script>
    let NewDescription = "";
    let validDescription = false;
    $: validDescription = NewDescription.trim().length >= 5; // declaração reativa
</script>

<div class="container">
    <div class="notification">
        <!-- Form -->
        <div class="field is-horizontal">
            <div class="field-label is-normal">
                <label class="label">Task</label>
            </div>
            <div class="field-body">
                <div class="field">
                    <p class="control is-expanded has-icon-left">
                        <input id="NewDescriptionId" bind:value={NewDescription} class="input" type="text" placeholder="Enter new task..." />
                        <span class="icon is-small is-left">
                            <i class="fas fa-tasks" />
                        </span>
                    </p>
                </div>
                <!-- Buttons -->
                <div class="field is-grouped">
                    <div class="control">
                        <button class="button is-normal">New</button>
                    </div>
                    <div class="control">
                        <button class="button is-info" disabled={ !validDescription }>
                            <span class="icon is-small">
                                <i class="fas fa-check" />
                            </span>
                            <span>Save</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
        <!-- Binding -->
        <div class="field is-horizontal adding-record">
            <div class="field label">New record:</div>
            <div class="field body">
                <div class="field">
                    <div class="control">{NewDescription}</div>
                </div>
            </div>
        </div>
    </div>
</div>