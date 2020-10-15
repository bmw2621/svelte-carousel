<script>
	import Carousel from './components/Carousel.svelte';
	import { ChevronLeftIcon, ChevronRightIcon } from 'svelte-feather-icons';

	const images = [
		{path: 'images/image1.jpg', id: 'image1'},
		{path: 'images/image2.jpg', id: 'image2'},
		{path: 'images/image3.jpg', id: 'image3'},
		{path: 'images/image4.jpg', id: 'image4'},
		{path: 'images/image5.jpg', id: 'image5'},
		// {path: 'images/image6.jpg', id: 'image6'},
	]
</script>


<Carousel
	{images}
	imageWidth={250}
	imageSpacing={15}
	controlColor={'white'}
	controlScale={0.8}/>

<style>

</style>
