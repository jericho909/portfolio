<script>
    import Step from "./Step.svelte";
    let steps = [
        {name: 'Tourism Agency Management', icon: 'fa-solid fa-shield-dog'},
        {name: 'Veterinary Management System', icon: 'fa-solid fa-hotel'},
        {name: 'Random Password Generator', icon: 'fa-solid fa-lock'}
    ]

    let benefits = [
        {name: "a lawyer turned software developer", description: "My background in law provides me with a unique perspective on problem-solving and attention to detail. I am adept at analyzing complex information, drafting precise documents, and adhering to strict deadlines. These skills translate seamlessly into software development, where accuracy and efficiency are paramount."},
        {name: "an excellent communicator", description: "Having served as a partner attorney and founding attorney in legal firms, I have honed my communication skills through client interactions, negotiations, and courtroom presentations. This experience translates into effective communication within software development teams, fostering collaboration, clarity, and efficiency in project execution."},
        {name: "continuous learner", description: "Driven by a passion for technology and a commitment to professional growth, I thrive in dynamic environments where learning is ongoing. Whether mastering new programming languages or staying abreast of industry trends, my adaptive learning mindset empowers me to quickly acquire new skills and adapt to the ever-changing demands of the software development landscape."}
    ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"> 
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Ömer Ahmet</span> Yücel.<br/> Full Stack <span class="poppins text-violet-400">Developer.</span>
            </h2>
            <p class="text-base sm:text-lg md.text-xl">
                My <span class="text-violet-400">favorite tech</span> includes Java (Spring Boot), JavaScript (Svelte or React), TailwindCSS, PostgreSQL!
            </p>
            <a href="https://www.linkedin.com/in/omerahmetyucel/" target="_blank" class="blueShadow mx-auto lg:auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 rounded-full bg-white text-slate-950 cursor-pointer">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200">

                </div>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
    </section>




    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my projects
            </h6>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={{...steps[0], href:"https://github.com/jericho909/hotel_management"}}>
                <p>The Tourism Agency Management System is a Full Stack CRUD application that helps agencies by streamlining hotel partnerships, optimizing customer reservations, and enabling efficient user and hotel management. It utilizes <strong class="text-violet-400">Java</strong> for both frontend and backend, with <strong class="text-violet-400">Swing UI</strong> for the frontend and <strong class="text-violet-400">PostgreSQL</strong> for the database.</p>
            </Step>
            <Step step={{...steps[1], href: "https://github.com/jericho909/veterinary"}}>
                <p>The Veterinary Management System project, built with <strong class="text-violet-400">Java Spring Boot</strong>, offers a robust API for efficiently managing veterinary clinic operations. It includes features such as animal and customer management, vaccine administration tracking, appointment scheduling, and veterinary doctor management. With <strong class="text-violet-400">Spring Web, Spring Data JPA, and PostgreSQL</strong>, it provides a seamless experience for veterinary clinics to streamline their processes.</p>
            </Step>
            <Step step={{...steps[2], href: "https://jericho909.github.io/randompassword/"}}>
                <p>The Random Password Generator web app, constructed with <strong class="text-violet-400">HTML, CSS</strong> and <strong class="text-violet-400">JavaScript</strong>, enables users to effortlessly create random passwords tailored to their preferences. With a user-friendly interface allowing customization of password length and one-click copying to the clipboard, it offers a convenient solution for generating secure passwords.</p>
            </Step>
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700
        after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl"> Want to know more? </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">A bit <span class="poppins text-violet-400">about</span> me.</h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
           {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>