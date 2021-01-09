<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Example Component</div>

                    <div class="card-body">
                        I'm an example component.11
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted() {
            window.Echo.channel('notification-event')
                .listen('NotificationEvent', (e) => {
                    alert(`title: ${e.title} , message: ${e.message}`)
                });
        }
    }
</script>
