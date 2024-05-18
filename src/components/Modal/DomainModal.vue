<script setup>

import IconEmail from '@/components/icons/IconEmail.vue'

const emit = defineEmits(['closeModal'])
function closeModal() {
    emit('closeModal', false);
}
</script>
<template>
    <div id="modal" class="modal">
        <div class="modal-content">
            <!-- HEADER -->
            <div class="model-header">
                <h2>Custom Domain</h2>

                <span @click="closeModal" class="close-button">&times;</span>
            </div>

            <div class="model-body">
                <div class="model-body__content">

                    <div class="content-steps">
                        <span class="step">
                            1
                        </span>
                        <div class="content-steps__elements">

                            <p>Add your email</p>

                            <div class="content-steps-elements__actions">
                                <input placeholder="jhondoe@gmail.com" type="text">
                                <button>Generate DNS Records</button>
                            </div>
                        </div>
                    </div>


                    <div class="content-steps">
                        <span class="step">2</span>
                        <div class="gap-16">
                            <div class="gap-8">
                                <p>Get started authenticating your domain</p>
                                <p class="description">From your domain provider’s website, find the page or area that
                                    has
                                    your domain or domain records - usually called manage domain, DNS custom records or
                                    zone
                                    files.</p>
                            </div>

                            <div style="display: flex; justify-content: space-between;">
                                <p style="margin: auto 0;">Need detailed guide of how to do it?</p>
                                <div class="domain-provider-badge">
                                    <span>Select your domain provider</span>
                                    <div class="dropdown-arrow"></div>
                                </div>
                            </div>
                        </div>
                    </div>


                    <div class="content-steps">
                        <span class="step">3</span>
                        <div class="gap-24">
                            <div class="gap-8">
                                <p>Get started authenticating your domain</p>
                                <p class="description">You are going to add two CNAME records to your domain on your
                                    domain
                                    provider’s website. They give Vanilla permission to send emails on your behalf by
                                    authenticating this domain</p>
                            </div>
                            <div class="email-list">
                                <IconEmail />
                                <div>
                                    <p>Add your email address</p>
                                    <p class="description">To get a DNS records, you need to add your email address
                                        first</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

            </div>

            <div class="model-footer">
                <div class="model-footer__buttons">
                    <button class="status-button" @click="closeModal">Check Status</button>
                    <button class="save-button" @click="closeModal">Save Changes</button>
                </div>
            </div>


        </div>
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');

.modal {
    position: fixed;
    font-family: "Inter";
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.4);
    backdrop-filter: blur(8px);
}

.modal-content {
    background-color: #fefefe;
    margin: 6% auto;
    border-radius: 16px;
    font-family: inherit;
    width: 860px;
    border-radius: 16px;
    border: 1px solid rgba(0, 11, 54, 0.09);

}

.gap-8 {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.gap-16 {
    display: flex;
    flex-direction: column;
    gap: 16px;

}

.gap-24 {
    display: flex;
    flex-direction: column;
    gap: 24px;
}

.close-button {
    color: #1E1F24;
    font-size: 18px;
    margin: auto 0;
    font-weight: bold;
}

.close-button:hover,
.close-button:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
}

.model-header {
    display: flex;
    justify-content: space-between;
    color: #1E1F24;
    padding: 16px 20px;


}

.model-header h2 {
    color: #1E1F24;
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
    line-height: 24px;
}

.model-body {
    width: 100%;
    border-top: 1px solid rgba(0, 11, 54, 0.09);
    border-bottom: 1px solid rgba(0, 11, 54, 0.09);
}

.model-body__content {
    padding: 20px;
    display: flex;
    flex-direction: column;
    gap: 24px;

}

.step {

    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 24px;
    height: 24px;
    border-radius: 50%;
    font-family: "Inter";
    color: rgba(0, 1, 7, 0.88);
    background: rgba(0, 16, 64, 0.06);
    font-size: 12px;
    font-style: normal;
    font-weight: 500;
    color: rgba(0, 1, 7, 0.88);
    line-height: 16px;
}


.content-steps {
    display: flex;
    flex-direction: row;
    gap: 16px;

}

.content-steps__elements {
    display: flex;
    flex-direction: column;
    font-family: "Inter";
    width: 100%;
    gap: 6px;
}

p {
    margin-block-start: 0;
    margin-block-end: 0;
    color: #1E1F24;
    font-size: 14px;
    font-family: "Inter";
    font-style: normal;
    font-weight: 500;
    line-height: 20px;
}

.description {
    margin-block-start: 0;
    margin-block-end: 0;
    color: #62636C;
    font-family: "Inter";
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 20px;

}

.domain-provider-badge {
    display: inline-flex;
    align-items: center;
    padding: 8px 16px;
    background-color: white;
    border-radius: 8px;
    border: 1px solid rgba(0, 7, 53, 0.15);
    background: rgba(255, 255, 255, 0.00);
}

.domain-provider-badge span {
    font-family: "Inter";
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 20px;
    color: rgba(0, 2, 17, 0.62);
}

.dropdown-arrow {
    width: 0;
    height: 0;
    border-left: 5px solid transparent;
    border-right: 5px solid transparent;
    border-top: 5px solid #888;
    margin-left: 14px;

}

.email-list {
    padding: 16px;
    border-radius: 12px;
    border: 1px dashed rgba(0, 11, 54, 0.09);
    display: flex;
    flex-direction: row;
    gap: 16px;
    margin-bottom: 52px;
}

.content-steps-elements__actions {
    display: flex;
    flex-direction: column;
    gap: 16px;

}

.content-steps-elements__actions input {
    border-radius: 8px;
    border: 1px solid rgba(0, 7, 53, 0.15);
    background: rgba(255, 255, 255, 0.00);
    height: 40px;
    padding: 0 10px;
    font-family: "Inter";
}

.content-steps-elements__actions input::placeholder {
    overflow: hidden;
    color: rgba(0, 2, 17, 0.62);
    font-family: "Inter";
    text-overflow: ellipsis;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: 20px;
}

.content-steps-elements__actions button {
    width: max-content;
    border-radius: 6px;
    background: rgba(0, 16, 64, 0.06);
    border: none;
    font-family: "Inter";
    display: flex;
    height: 32px;
    padding: 0px 12px;
    justify-content: center;
    align-items: center;
    gap: 4px;
    color: #1E1F24;
    font-size: 14px;
    font-weight: 500;
    line-height: 20px;
    cursor: pointer;
}



.model-footer__buttons {
    display: flex;
    justify-content: flex-end;
    margin: 16px 20px;
    gap: 8px;
}


.status-button {
    color: #1E1F24;
    font-size: 14px;
    font-style: normal;
    font-family: "Inter";
    font-weight: 500;
    line-height: 20px;
    background: transparent;
    padding: 0 12px;
    border-radius: 8px;
    height: 40px;
    border: 1px solid rgba(0, 7, 53, 0.15);
    cursor: pointer;

}

.save-button {
    padding: 0px 12px;
    height: 40px;
    border-radius: 8px;
    font-family: "Inter";
    background: #1E1F24;
    color: #FCFCFD;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: 20px;
    cursor: pointer;
}
</style>