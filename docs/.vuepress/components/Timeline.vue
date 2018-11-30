<template>
	<ul
		v-if="items.length"
		class="timeline"
	>
		<li
			v-for="(item, index) in items"
			:key="index"
			class="timeline-item"
		>
			<div
				class="timeline-panel"
				:class="{
					'current': item.status === 'pending'
				}"
			>
				<div class="timeline-heading">
					<h4 class="timeline-title">{{ item.title }}</h4>
					<div class="timeline-panel-date">
						<div class="timestamp">
							<small class="text-muted">
								{{ item.date }}
							</small>
						</div>
					</div>
				</div>
				<div
					v-html="md(item.body)"
					class="timeline-body"
				/>
			</div>
		</li>
	</ul>
</template>

<script>
	import Vue from 'vue';

	export default Vue.extend({
		name: 'Timeline',
		data() {
			return {
				statuses: {
					done: {
						icon: 'check',
						color: 'success'
					},
					pending: {
						icon: 'visibility',
						color: 'primary'
					},
					next: {
						icon: 'schedule',
						color: 'info'
					}
				}
			}
		},
		methods: {
			md(input) {
				return input.replace(/__(.*?)__((_+|\W+|$))/g, '<strong>$1</strong>$2');
			}
		},
		props: {
			items: {
				type: Array,
				required: true
			}
		}
	});
</script>
