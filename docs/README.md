# Issue #1043

The issue is when using the `ClientOnly` component.

`TimeLine` is the component from my project, slightly updated.

## No tabs

Works.

<ClientOnly>
<Timeline
	:items="[
		{
			status: 'done',
			date: 'November 2018',
			title: 'v1.4 Release',
			body: 'Use __Vue plugin architecture__, improve documentation refactor __BirthDatepicker__, improve existing components, add __TypeScript typings__ and __release script__.'
		},
		{
			status: 'pending',
			date: 'November 2018',
			title: 'v1.5 Release',
			body: 'Add __themes__ and __reduce lib size__ to fit under 200ko.'
		},
		{
			status: 'next',
			date: 'December 2018',
			title: 'v1.5.x Releases',
			body: 'Add __documentation__ for __DatePicker__ and add __ListField__ component.'
		},
		{
			status: 'next',
			date: 'Q1 2019',
			title: 'v1.6 Release',
			body: 'Add __File Upload/Download__ and __Address__ components.'
		},
		{
			status: 'next',
			date: 'Q2 2019',
			title: 'v1.6.x Releases',
			body: '100% __tests coverage__.'
		}
	]"
/>
</ClientOnly>

## Tabs

Oops!

<ClientOnly>
	<Timeline
		:items="[
			{
				status: 'done',
				date: 'November 2018',
				title: 'v1.4 Release',
				body: 'Use __Vue plugin architecture__, improve documentation refactor __BirthDatepicker__, improve existing components, add __TypeScript typings__ and __release script__.'
			},
			{
				status: 'pending',
				date: 'November 2018',
				title: 'v1.5 Release',
				body: 'Add __themes__ and __reduce lib size__ to fit under 200ko.'
			},
			{
				status: 'next',
				date: 'December 2018',
				title: 'v1.5.x Releases',
				body: 'Add __documentation__ for __DatePicker__ and add __ListField__ component.'
			},
			{
				status: 'next',
				date: 'Q1 2019',
				title: 'v1.6 Release',
				body: 'Add __File Upload/Download__ and __Address__ components.'
			},
			{
				status: 'next',
				date: 'Q2 2019',
				title: 'v1.6.x Releases',
				body: '100% __tests coverage__.'
			}
		]"
	/>
</ClientOnly>
