OQMD/qmpy v1.3 release
======================

TODO
----

1. - [ ] @[Mohan](https://github.com/mohanliu) The 3d phase diagram on the home page: can we use Helvetica? And may be place
   the labels so that they don't overlap with the phases (just add a +dx, +dy to
   the coordinates of the text)
2. - [ ] @[Jiahong](https://github.com/WalterjhShen) Some of the shortcut labels on the home page are not very helpful: e.g. the
   difference between ``Search Materials Phases`` and ``Browse Material
   Properties`` are not clear.  In fact, I'm not even sure that the labels are
   accurate. The second link, I'd say, is to ``filter/screen`` materials based
   on some property. The first link can also be used to search for entire phase
   diagrams. This can be discussed with the rest of the group + Chris.
3. - [ ] @[Abi](https://github.com/tachyontraveler) Adding to my note above, the GCLP shortcut needs to have ``GCLP`` somewhere
   in the description. And API needs to be ``REST API`` or ``RESTful API``.
4. - [ ] @[Abi](https://github.com/tachyontraveler) Last thing about the shortcuts on the home page (I'm being annoying about the
   home page because it is the HOME page; everyone who visits OQMD will visit
   it): we need to have mouse over for the shortcut links that have a one-line
   description of where the link will take them.
5. - [ ] @[Abi](https://github.com/tachyontraveler) Whatever link descriptions we choose to go with in 3./4. above, we can also
   use on this page: http://oqmd.org:8080/materials/
6. - [ ] @[Jiahong](https://github.com/WalterjhShen) The GCLP page (http://oqmd.org:8080/analysis/gclp/): can we update the
   cryptic and nearly useless description on the webpage (take a look at any of
   the papers from the group that uses/describes GCLP)? Also format the two
   references properly, provide links, etc.
7. - [ ] @[Abi](https://github.com/tachyontraveler) The phase diagrams page (http://oqmd.org:8080/analysis/phase_diagram). Same
   comment as for GCLP above. Both for this page and the GCLP page, we need to
   give users information that helps them use the page/tools correctly. We can
   remove the FERE reference, formation energy information (or at least move it
   to the calculation settings page).
8. - [ ] @[Jiahong](https://github.com/WalterjhShen) The DFT settings page (http://oqmd.org:8080/documentation/vasp). Can we
   rename this page to ``Calculation details``? Update it with the "new"
   relaxation scheme, add a note about how formation energies are calculated
   with elemental chemical potentials corrections (and GGA/GGA+U compatibility
   corrections). Add a link to the list of elemental chemical potentials, the
   GGA/GGA+U corrections, and information about the sources of experimental
   formation energy used in the OQMD.
9. - [ ] @[Jiahong](https://github.com/WalterjhShen) The structure sources page (http://oqmd.org:8080/documentation/structures).
   Update this page to include the new number of entries calculated, and the
   new prototypes that have been (at least partially) calculated.
10. - [ ] @[Abi](https://github.com/tachyontraveler) The API landing pages (both OQMDAPI and Optimade API) take the user directly
    to the corresponding ``data`` pages. Can we have a more graceful landing
    pages for both? For example, the OQMDAPI link should take the user to
    http://oqmd.org/oqmdapi, and not
    http://oqmd.org:8080/oqmdapi/formationenergy. The former link shouldn't just
    be a wall of data but may instructions on how to use the API (copying the
    corresponding info from the documentation in very a condensed form is OK).
    For example, see the Materials Project API landing page:
    https://materialsproject.org/open. This should be true for both OQMD API and
    Optimade API.
11. - [ ] @[Abi](https://github.com/tachyontraveler) The documentation here (http://oqmd.org:8080/static/docs/restful.html) does
    not explain the difference between the two REST APIs. Can we separate the
    two in the documentation in a way that makes sense please?
12. - [ ] @[Abi](https://github.com/tachyontraveler) The "installation" step in the qmpy docs
    (http://oqmd.org:8080/static/docs/index.html) need updating. We should be
    recommending users to use ``(mini)conda`` for setting up and using qmpy for
    a uniform experience. There is a lot to change in the rest of the
    documentation as well but we can do it incrementally (i.e. those other
    changes need not be the limiting factor blocking this release).
13. The composition page (e.g. http://oqmd.org:8080/materials/composition/SiC):
    - [ ] @[Jiahong](https://github.com/WalterjhShen)rows can be: ``Ground state phase(s)``, ``Hull energy`` (not \Delta H!),
      ``Decomposition energy``, ``Competing phases``, ``Experimental formation
      energy``. Please iterate with others in the group + Chris
    - [ ] @[Abi](https://github.com/tachyontraveler) remove background highlight for ``Stable Phase`` (and correspondingly for
      ``Unstable Phase``, like Eric mentioned on the Slack channel). We need not
      emphasize either stable or unstable phases. That's why I said, remove
      background highlight, and if you really want to have color, just change
      the font color.)
    - [ ] @[Jiahong](https://github.com/WalterjhShen) I like the "?" for hull distance (the schematic that pops up; I don't like
      pop ups in general and don't understand why it cannot be just a page under
      ``Calculation details``), but the schematic needs quite a bit of
      improvement to be clearer/less confusing. E.g. What is E_f, and what is
      \Delta H? I understand you're referring to formation energy and hull
      energy. But "hull energy" is not a physical quantity that we are plotting.
      The y-axis has to be r"Formation energy $\Delta E_{\rm f}$". Hull energy
      at a given composition can be "$E_{\rm hull}$". And so on. Please discuss
      this with Eric/Chris/others in the group to finalize. (And feel free to
      ping me on Slack. I don't want to plug my own paper but see Page 5 here
      https://arxiv.org/pdf/1610.02444.pdf for the terminology/symbols.)
    - [ ] @[Abi](https://github.com/tachyontraveler) why are entire rows not clickable anymore? only the ``ID`` column being
      clickable is really cumbersome, please change it back.
14. The entry page (e.g. http://oqmd.org:8080/materials/entry/1239872):
    - [ ] @[Mohan](https://github.com/mohanliu) can we have similar data as the composition page, i.e. the hull distance,
      stability, etc. for each entry?
    - [ ] @[Mohan](https://github.com/mohanliu) can we go back to having just the ``static`` or ``standard`` calculation
      showing up in the ``Calculations`` table and have an optional
      ``Calculation History`` table that users can click to unravel?
    - [ ] @[Abi](https://github.com/tachyontraveler) same comment about table rows not being clickable? why?! please change it
      back so that the entire row is clickable. (I think) you want to convey
      that users are clicking and navigating to the Entry/Calculation/etc. and
      not the space group or something, but this tiny entry ID being the only
      clickable column is very annoying.
15. - [ ] @[Mohan](https://github.com/mohanliu) The calculation page (e.g.
    http://oqmd.org:8080/analysis/calculation/2901446): can we have the default
    x-axis range for the DOS plot to be [-5, 5] or [-6, 6]?
16. - [ ] @[Abi](https://github.com/tachyontraveler) May be add a few questions to the FAQ? Such as ``how can find the reference
    for the experimental formation energy for compound XYZ?``, ``This compound
    is in the ICSD but OQMD says it is unstable``, and so on.

