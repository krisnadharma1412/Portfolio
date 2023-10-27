<script>
    import Step from "./Step.svelte"
    let steps = [
        {name: 'Maintenance Activity Monitoring Website', icon: 'fa-solid fa-chart-pie'},
        {name: 'Metatah Event Invitation', icon: 'fa-solid fa-envelope'},
        {name: 'CLI MyAnimeList', icon: 'fa-solid fa-list'}
    ]

    let benefits = [
        {
            name: "a self taught developer",
            description:
                "I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, cloud services and much much more.",
        },
        {
            name: "an excellent communicator",
            description:
                "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
        },
        {
            name: "a tech enthusiast and lifelong learner",
            description: "I am proactive in expanding my knowledge and am currently in the process of acquiring expertise in React and the Django framework. My eagerness to learn and adapt to new technologies reflects my commitment to staying current and enhancing my capabilities in the field.",
        }
    ];

    let btn_style = "mr-auto cursor-pointer hover:text-slate-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full after:w-full after:h-full after:duration-200 after:bg-white hover:after:translate-x-full after:z-[-1] overflow-hidden";
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Krisna</span> Dharma 
                <br>Software <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favorite tech</span> includes Javascript , Bootstrap, TailwindCSS, PHP (Laravel), Python,
                & MySQL
            </p>
            <a href="https://www.linkedin.com/in/i-putu-krisna-dharma-saputra-01084014b/" target="_blank" class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <!-- svelte-ignore a11y-img-redundant-alt -->
            <img src={"images/profile.png"} alt="Profile image" class="object-cover z-[2] max-h-[70vh]" />
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavors
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span>
                my work?
            </h3>
        </div>
        <a 
            href="https://github.com/krisnadharma1412"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white
            flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hoverr:border-violet-700 duration-200"
        ><i class="fa-brands fa-github fa-bounce"></i>
         <p>See my GitHub</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-18">
            <Step step={steps[0]}>
                <p>A project to monitoring the process of handling software errors at Polytron 
                    so that the system team can monitor the progress in handling case reports by the developer team and the system team itself more easily. 
                    Created with <strong class="text-violet-400">HTML, CSS, PHP, Laravel, Bootstrap, Javascript, JQuery, AJAX, and MySQL</strong>
                </p>
                <img src="images/maintenance.jpg" alt="maintenance project img">
                <div class="flex-1 flex justify-between gap-4 items-center">
                    <div class={btn_style}>
                        <a href='https://docs.google.com/presentation/d/1ZR9aIMrB_0SM-H-J84-FW9n2B_3RbPAQkPH4wxVtIcU/edit#slide=id.g242348421c2_0_24' target="_blank" class="relative z-4"><i class="fa-regular fa-folder-open"></i> Documentation</a>
                    </div>
                </div>
            </Step>
            <Step step={steps[1]}>
                <p>This is an online invitation website i developed for my sister's and my metatah event.
                    Metatah/Mepandes ceremony in Bali is a significant cultural and religious event that signifies the transition from childhood to adolescence and the deeper commitment to the Balinese Hindu faith. 
                    Created with <strong class="text-violet-400">HTML, CSS, Bootstrap, and Javascript</strong>
                </p>
                <img src="images/metatah.png" alt="metatah invitation img">
                <div class="flex-1 flex justify-between gap-4 items-center">
                    <div class={btn_style}>
                        <a href='https://github.com/krisnadharma1412/Metatah-Invitation' target="_blank" class="relative z-4"><i class="fa-solid fa-code"></i> Repository</a>
                    </div>
                    <div class={btn_style}>
                        <a href='https://krisnadharma1412.github.io/Metatah-Invitation/' target="_blank" class="relative z-4"><i class="fa-solid fa-desktop"></i> Demo</a>
                    </div>
                </div>
            </Step>
            <Step step={steps[2]}>
                <p>CLI MyAnimeList is a program where you can create a list of anime that you want to watch just like in https://myanimelist.net/ website,
                    and create a Tier List of anime from S tier to E tier in PNG image from your list.
                    Created with <strong class="text-violet-400">Python, Jikan REST API, JSON</strong>
                </p>
                <img src="images/myanimelist.png" alt="cli myanimelist img">
                <div class="flex-1 flex justify-between gap-4 items-center">
                    <div class={btn_style}>
                        <a href='https://github.com/krisnadharma1412/MyAnimeList-in-Python-CLI' target="_blank" class="relative z-4"><i class="fa-solid fa-code"></i> Repository</a>
                    </div>
                </div>
            </Step>
        </div>
    </section>

    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col
    gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700
         after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am ...
        </p>
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
        <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
            My Tech <span class="text-violet-400">Skills</span>
        </h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class={"border-b border-solid border-slate-200  "}>
                    <tr class="">
                        <th class="whitespace-nowrap p-2 px-4">Programming Language</th>
                        <th class="whitespace-nowrap p-2 px-4">Framework & Libraries</th>
                        <th class="whitespace-nowrap p-2 px-4">Database</th>
                        <th class="bg-violet-700 text-white whitespace-nowrap p-4 px-8">Other Dev Tools</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">
                            <i class="fa-solid fa-javascript"></i>
                        </td>           
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Laravel</td>
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">MySQL</td>
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">GIT</td>
                    </tr>
                    <tr>
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">PHP</td>
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Bootstrap</td>
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">SQL Server</td>
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">AJAX</td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Python</td>
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">TailwindCSS</td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"></td>
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">JQuery</td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am currently open to <span class="text-violet-400">full time, and internship onsite/remote</span> job opportunities and freelance projects.
        </p>
    </section>
</main>