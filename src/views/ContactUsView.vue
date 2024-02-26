<script>
    export default {
    name: "ContactUsView"
    }
</script>

<template>
    <div class="container mt-3">
        <div class="row justify-content-center ">
            <div class="col-12">
                <h1 class="text-center">
                    Contact Us
                </h1>
            </div>
            <div class="col-10">
                <form>
                    <div class="mb-3">
                        <label for="name" class="form-label">Name</label>
                        <input type="text" class="form-control" id="name">
                    </div>
                    <div class="mb-3">
                        <label for="email" class="form-label">Email</label>
                        <input type="email" class="form-control" id="email">
                    </div>
                    <div class="mb-3">
                        <label for="message" class="form-label">Message</label>
                        <textarea class="form-control" id="message" rows="5"></textarea>
                    </div>
                    <div class="mb-3">
                        <button type="button" class="btn btn-primary">Send</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>