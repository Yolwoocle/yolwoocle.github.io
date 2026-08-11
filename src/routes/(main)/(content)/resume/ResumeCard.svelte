<script lang="ts">
    export let title: string;
    export let subtitle: string;
    export let period: string;
    export let stickerRound: boolean = true;
    export let stickerImg: string = "";
    export let stickerAlt: string = "";

    let randomRotation = (Math.random() * 2 - 1) * 0.15
</script>

<div class="relative flex flex-col bg-white items-center rounded-2xl pt-4 pb-4 px-4 shadow-[2px_8px_0px_var(--transp-shad)]">
    <div class="flex flex-row w-full justify-between gap-4">
        <div class="flex flex-col text-left">
            <h3 class="font-black text-2xl pb-2">{title}</h3>
            <p class="text-m">
                📍 <strong>{subtitle}</strong>
            </p>
            <p class="text-m">
                🗓️ {period}
            </p>
        </div>
        {#if stickerImg}
            <div 
                class="size-18 shrink-0 aspect-square overflow-hidden shadow-[1px_3px_0px_var(--transp-shad)]"
                class:rounded-full={stickerRound}
                class:rounded-xl={!stickerRound}
                // style={`transform: rotate(${randomRotation}rad)`}
            >
                <img class="overflow-hidden" src={stickerImg} alt={stickerAlt}/>
            </div>
        {/if}
    </div>
    <div class="text-l w-full text-left pt-4">
        <slot />
    </div>
</div>
