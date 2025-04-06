<script lang="ts">
    import * as Card from "$lib/components/ui/card/index.js";
    import * as Carousel from "$lib/components/ui/carousel/index.js";

    
	let items = [
		{ img: 'https://i.pinimg.com/736x/87/06/78/870678092446e8350a689170e5a76368.jpg' },
		{ img: 'https://i.pinimg.com/736x/c0/69/8e/c0698edb6555bafff66d0140537428c7.jpg' },
		{
			img: 'https://i.pinimg.com/736x/47/34/29/4734299f643adced363d56a37de743ec.jpg'
		},
		{
			img: 'https://i.pinimg.com/736x/3f/9d/98/3f9d9899f386b6ac008e2dd587eeea80.jpg'
		},
      {
         img: 'https://i.pinimg.com/736x/c6/92/c8/c692c83f10be9be50ed70e0f7ea3c677.jpg'
      }
	];
   </script>
    
   <Carousel.Root class="w-full max-w-xs">
    <Carousel.Content>
     {#each items as i}
      <Carousel.Item>
       <div class="p-1">
        <Card.Root>
         <Card.Content
          class="flex aspect-square items-center justify-center p-6"
         >
          <img src={i.img} alt="">
         </Card.Content>
        </Card.Root>
       </div>
      </Carousel.Item>
     {/each}
    </Carousel.Content>
    <Carousel.Previous />
    <Carousel.Next />
   </Carousel.Root>